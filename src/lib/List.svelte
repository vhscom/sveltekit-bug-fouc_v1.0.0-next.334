<script>
  import ListItems from "./ListItems.svelte";

  /** @type any[] */
  export let items;

  /** @type string */
  export let name;
</script>

<ul>
  {#each items as item (item.name)}
    <li>
      <h2>{name}</h2>
      <ul>
        <ListItems items={item.children} name={item.name} />
      </ul>
      {item.content}
    </li>
  {/each}
</ul>

<style>
  h2 {
    font-size: small;
  }
</style>
