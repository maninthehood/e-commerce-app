<script>
let products = [
    {
        id: 1,
        name: "Iphone 14 Pro Max",
        img: "https://fdn2.gsmarena.com/vv/pics/apple/apple-iphone-14-pro-max-1.jpg",
        price: 999,
        bought: false
    },
        {
        id: 2,
        name: "Iphone 13 Pro Max",
        img: "https://www.apple.com/newsroom/images/product/iphone/standard/Apple_iphone13_hero_09142021_inline.jpg.slideshow-xlarge_2x.jpg",

        price: 599,
        bought: false
    },
        {
        id: 3,
        name: "Iphone 12 Pro Max",
        img: "https://cdn.dxomark.com/wp-content/uploads/medias/post-62960/iPhone-12-Hero.png",
        price: 899,
        bought: false
    },
]

let bought = []


</script>
<main>
{#each products as product}
    <div>
        <div>
        <img src={product.img} alt="">
        </div>
    </div>
{/each}
</main>

<style>
    main{
        position: relative;
        margin-bottom:100vh;
    }

    @media (max-width: 800px){
        img{
            margin-top:20px;
            margin-left:20px;
            height:200px;
            width:200px;
        }
    }

</style>