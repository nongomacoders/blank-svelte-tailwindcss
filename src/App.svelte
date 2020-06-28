<script>
  import Modal from "./Modal.svelte";
  import {showModal} from "./stores.js";
</script>

<p>
  Lorem ipsum dolor sit amet consectetur, adipisicing elit. Voluptatum unde
  consequuntur, cum fugit deleniti asperiores, reiciendis impedit est rerum
  quisquam quo eaque placeat, facilis sit laborum neque dolorem officia.
  Nostrum.
</p>
{#if $showModal}
	<Modal>hello</Modal>
{/if}
<button on:click={()=>showModal.set(1)}>Show modal</button>

