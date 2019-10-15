<script context="module">
	export function preload({ params, query }) {
		return this.fetch(`blog.json`).then(r => r.json()).then(posts => {
			return { posts };
		});
	}
</script>

<script>
  import { onMount } from 'svelte';
 // import { basePath } from '../../config';
  //import { ProductService } from '../../services/product.service';
 // import { Product } from '../../interfaces/Product';

  export let products=[];

  onMount(() => {
       /* fetch(basePath + '/api/SampleData/WeatherForecasts')
            .then(response => response.json())
            .then(data => {
                forecasts = data;
            });

            this.fetch(`blog.json`)
            .then(r => r.json())
            .then(posts => {
               return { posts };
            } 
            */
            products=getProducts();  
            console.log(products);  
            
    });

  function getProducts(){
    /*this.productService.getProducts()
      .subscribe(
        res => this.products = res,
        err => console.log(err)
      )*/
      console.log('getProducts');
      return [{
        _id: '1',
         name: 'TABLET',
         description: 'TABLET 180',
         price: 100,
         createdAt: '01/01/2019'
      },
      {
        _id: '2',
         name: 'PC',
         description: 'COMPUTADOR 180',
         price: 150,
         createdAt: '01/01/2019'
      }
    ];

  }

  function deleteProduct(id) {
    /*this.productService.deleteProduct(id)
      .subscribe(
        res => {
          console.log(res);
          this.getProducts();
        },
        err => console.log(err)
      )
      */
      console.log('produto excluido '+id);
  }

</script>

{#each products as product}
<div class="card card-body mb-2">
  <div class="row">
    <div class="col-md-8">
      <ul>
        <li>
          id: {product._id}
        </li>
        <li>
          name: {product.name}
        </li>
        <li>
          description: {product.description}
        </li>
        <li>
          price: {product.price}
        </li>
        <li>
          createdAt: {product.createdAt}
        </li>
      </ul>
      <button on:click="{() => deleteProduct(product._id)}" class="btn btn-danger">
        Delete
      </button>
      <button href="/product-form/edit/{product._id}" class="btn btn-secondary">
        Edit
      </button>
    
    </div>
    <div class="col-md-4">
      <!--<img [src]="{product.imageURL}" class="card-img"> -->
    </div>
  </div>
</div>
{/each}