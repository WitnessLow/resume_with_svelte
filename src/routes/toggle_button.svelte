<!-- ToggleButton.svelte -->

<script>
  let showContacts = false;

  function toggleContacts() {
    showContacts = !showContacts;
  }
</script>
  
  <style>
    /* You can add styles for your button here */
    .toggle-btn {
      cursor: pointer;
      padding: 10px;
      background-color: #3490dc;
      color: #fff;
      border: blue;
      border-radius: 5px;
    }
  </style>
  
  <button on:click={toggle} class="toggle-btn">
    {#if isToggled}
      Toggled ON
    {:else}
      Toggled OFF
    {/if}
  </button>
  