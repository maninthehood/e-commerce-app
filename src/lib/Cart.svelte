<script context="module">
export let showCart = false;
export function toggleCart(){
    showCart = !showCart;
}
</script>

<main>
    {#if showCart}
        <div>Cart Component</div>
    {/if}
</main>



