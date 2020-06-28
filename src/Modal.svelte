<script>
import Button from './Button.svelte'
 import {showModal} from "./stores.js";
function closeModal(){
showModal.set(0);
}
</script>

<style>


  .modal {
    position: fixed;
    top: 0;
    left:0;    
    width: 100%;
    max-height: 80vh;
    background: white;
    
    z-index: 100;
 
    overflow: scroll;
  }

  h1 {
    padding: 1rem;
    margin: 0;
    border-bottom: 1px solid #ccc;
    font-family: "Roboto Slab", sans-serif;
  }

  .content {
    padding: 1rem;
  }

  footer {
    padding: 1rem;
  }

  @media (min-width: 768px) {
    .modal {
      width: 40rem;
      left: calc(50% - 20rem);
    }
  }
</style>



<div class="modal">
  <span>Edit</span><Button on:click={closeModal}>Close</Button>
  <div class="content">
    <slot />
  </div>
  <footer>
    <slot name="footer">
      <Button on:click={closeModal}>Close</Button>
    </slot>
  </footer>
</div>