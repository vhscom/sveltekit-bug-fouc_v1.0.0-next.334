<script>
  import List from "./List.svelte";

  /** @type any[] */
  export let items;

  /** @type string */
  export let name;
</script>

{#each items as item (item.name)}
  <li>
    <h3>{name}</h3>
    {#if item.children}
      <List items={item.children} name={item.name} />
    {/if}
    {item.content}
  </li>
{/each}
