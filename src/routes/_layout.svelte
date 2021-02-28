<script>
  import Sidebar from '../components/sidebar/Sidebar.svelte';
  import Nav from "../components/navbar/Nav.svelte";
</script>

<main class="flex flex-col h-screen w-full bg-gray-300">
  <div class="flex flex-row flex-auto">
    <Sidebar />
    <div class="flex flex-col bg-gray-500 w-full">
      <Nav />
      <slot />
    </div>
  </div>
  <div class="bg-gray-800 h-24 w-full">

  </div>
</main>