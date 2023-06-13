<script lang="ts">
    export let isOpen = false;
</script>

<div>
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <div
        class="fixed inset-0 bg-black opacity-25 z-40"
        hidden={!isOpen}
        on:click={() => (isOpen = false)}
    />

    <div
        class="fixed h-full w-64 bg-white shadow-lg z-50"
        class:translate-x-0={isOpen}
        class:-translate-x-full={!isOpen}
    >
 <ul class="py-4">
        <li class="px-4 py-2">
          <a href="/" class="block text-gray-300 hover:text-white">Home</a>
        </li>
        <li class="px-4 py-2">
          <a href="/" class="block text-gray-300 hover:text-white">About</a>
        </li>
        <li class="px-4 py-2">
          <a href="/" class="block text-gray-300 hover:text-white">Services</a>
        </li>
        <li class="px-4 py-2">
          <a href="/" class="block text-gray-300 hover:text-white">Contact</a>
        </li>
      </ul>
    </div>
</div>
