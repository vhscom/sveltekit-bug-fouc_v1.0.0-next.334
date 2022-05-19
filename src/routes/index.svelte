<script>
  import List from "$lib/List.svelte";

  const family = [
    {
      name: "Ketut",
      children: [
        {
          name: "Wayan",
          children: [
            {
              name: "Gede",
              children: [],
              content: "Gede content.",
            },
            {
              name: "Kadek",
              children: [
                {
                  name: "Putu",
                  children: [
                    {
                      name: "Nengah",
                      children: [],
                      content: "Nengah's content.",
                    },
                  ],
                  content: "Putu content.",
                },
              ],
              content: "Kadek content.",
            },
          ],
          content: "Wayan content.",
        },
      ],
      content: "Ketut content",
    },
  ];
  const [tree] = family;
</script>

<h1>Reproduction</h1>

<List items={tree.children} name={tree.name} />
