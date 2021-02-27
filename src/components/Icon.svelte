<script>
  import { onMount } from 'svelte';

  export let name;
  export let mode = 'outline';

  const url = 'https://raw.githubusercontent.com/tailwindlabs/heroicons/master/optimized/';

  onMount(async () => {
    const req = await fetch(`${url}${mode}/${name}.svg`);
    const content = await req.text();

    const el = document.getElementById('icon');
    el.innerHTML = content;

    const svg = el.children[0];
    svg.classList.add('h-6', 'w-6');

    if ($$props.class) svg.classList.add(...$$props.class.split(' '));
  });
</script>

<i id="icon"></i>