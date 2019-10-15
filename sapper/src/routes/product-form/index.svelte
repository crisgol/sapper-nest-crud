<script context="module">
    export function preload({ params, query }) {
      /*return this.fetch(`blog.json`).then(r => r.json()).then(posts => {
        return { posts };

      });
      */
      if (params.id) {
        /*this.productService.getProduct(params.id)
        .subscribe(
          res => {
            console.log(res);
            this.product = res;
            this.edit = true;
          },
          err => console.log(err)
        )*/
      }
    }
  </script>
  
  <script>
    import { onMount } from 'svelte';
   // import { basePath } from '../../config';
    //import { ProductService } from '../../services/product.service';
   // import { Product } from '../../interfaces/Product';
   
    let product = {
      name: '',
      description: '',
      imageURL: '',
      price: 0
    };
    
    let edit= false;


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
      //this.getProducts();    
    });

    function submitProduct() {
    /*this.productService.createProduct(this.product)
      .subscribe(
        res => {
          console.log(res);
          this.router.navigate(['/']);
        },
        err => console.log(err)
      )*/
  }

  function updateProduct() {
    /*delete this.product.createdAt;
    this.productService.updateProduct(this.product._id, this.product)
      .subscribe(
        res => {
          console.log(res);
          this.router.navigate(['/product'])
        },
        err => console.log(err)
      )*/
  }

</script>

<div class="row">
  <div class="col-sm-4 offset-sm-4">
    <div class="card card-body">

      <form on:submit={edit ? updateProduct() : submitProduct()}>

        <div class="form-group">
          <input type="text" name="name" bind:value="{product.name}" class="form-control" placeholder="Product Name" >
        </div>
        <div class="form-group">
          <input type="text" name="description" bind:value="{product.description}" class="form-control" placeholder="Description">
        </div>
        <div class="form-group">
          <input type="text" name="price" bind:value="{product.price}" class="form-control" placeholder="Price">
        </div>
        <div class="form-group">
          <input type="text" name="imageURL" bind:value="{product.imageURL}" class="form-control" placeholder="Image URL">
        </div>
        <button type="submit" class="btn btn-primary btn-block">
          Save
        </button>
      </form>
    </div>
  </div>
</div>