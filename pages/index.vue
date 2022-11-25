

<template>
    <div class="container">
        <div class="row">
            <div v-for="(product, index) in products" 
            :key="'product-' + index" 
            class="col-md-4">
                <div class="card mb-3">
                    <img :src="product.photoURL"
                     class="card-img-top">
                    <div class="card-body">
                        <h5 class="card-title">
                            {{ product.name }}
                        </h5>
                        <p class="card-text">
                            {{ product.description }}
                        </p>
                        <div class="d-grid">
                            <button @click="addToCart(product)" 
                            class="btn btn-outline-primary">
                                Add to cart
                            </button>
                            
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <ShoppingCart v-model="shoppingCart"/>
</div>
</template>
     

<script>
export default {
    data() {
        return {
            shoppingCart: [], // Store the added-to-cart items
            products: [
            {
                uuid: '5b9ed8b5-201e-4297-babb-29a566952e91',
                name: 'Camera model 1', 
                description: 'Lorem ipsum dolor sit amet.', 
                price: 2850,
                photoURL: 'https://images.pexels.com/photos/51383/photo-camera-subject-photographer-51383.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'
            },
            { 
                uuid: '973b3d42-e039-428a-b2ad-e6444b5895f4',
                name: 'Camera model 2', 
                description: 'Lorem ipsum dolor sit amet.', 
                price: 3100,
                photoURL: 'https://images.pexels.com/photos/1203803/pexels-photo-1203803.jpeg?auto=compress&cs=tinysrgb&dpr=3&h=750&w=1260'
            },
            {
                uuid: '33d3332e-42ac-4692-8523-ae76c3d8a773',
                name: 'Camera model 3', 
                description: 'Lorem ipsum dolor sit amet.', 
                price: 2150,
                photoURL: 'https://images.pexels.com/photos/249597/pexels-photo-249597.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'
            },
            { 
                uuid: 'c70080cd-330f-4398-b169-03f057582e2a',
                name: 'Camera model 4', 
                description: 'Lorem ipsum dolor sit amet.', 
                price: 2300,
                photoURL: 'https://images.pexels.com/photos/1091294/pexels-photo-1091294.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'
            },
            {
           
           uuid: 'c70080cd-330f-4398-b169-03f057582e2a',
           name: 'Camera model 5', 
           description: 'Lorem ipsum dolor sit amet.', 
           price: 2350,
           photoURL: 'https://live.staticflickr.com/65535/49690139461_55f0227ebc_b.jpg'
       },
       {
           
           uuid: 'c70080cd-330f-4398-b169-03f057582e2a',
           name: 'Camera model 6', 
           description: 'Lorem ipsum dolor sit amet.', 
           price: 1650,
           photoURL: 'https://i.pinimg.com/originals/38/3c/d7/383cd76bfc740107386e1d585cf590f5.jpg'
       },
       {
           
           uuid: 'c70080cd-330f-4398-b169-03f057582e2a',
           name: 'Camera model 7', 
           description: 'Lorem ipsum dolor sit amet.', 
           price: 1550,
           photoURL: 'https://favim.com/orig/201108/14/awesome-camera-cute-fisheye-photography-Favim.com-122696.jpg'
       },
       {
           
           uuid: 'c70080cd-330f-4398-b169-03f057582e2a',
           name: 'Camera model 8', 
           description: 'Lorem ipsum dolor sit amet.', 
           price: 1350,
           photoURL: 'https://th.bing.com/th/id/R.e3f35d51c545372395dcd3df0ed9f186?rik=rdakESlM0Myjrw&riu=http%3a%2f%2fs6.favim.com%2forig%2f65%2fbeautiful-camera-cute-floral-Favim.com-596436.jpg&ehk=lmxB3iNLqlHKBDRAj6pptrdtzUsQ8wGe15mVq6O1d3k%3d&risl=&pid=ImgRaw&r=0'
       },
            {
           
                uuid: 'c70080cd-330f-4398-b169-03f057582e2a',
                name: 'Camera model 9', 
                description: 'Lorem ipsum dolor sit amet.', 
                price: 2400,
                photoURL: 'https://th.bing.com/th/id/R.559177391a732339897fdcf4aaa93640?rik=FkfOhfn3teqR1w&riu=http%3a%2f%2fmcutiz.com%2fDSC01479.JPG&ehk=ROmIrxNWuppXLdyxIJ3eNWJ9%2bEHTashD%2bVR5vIKNTw4%3d&risl=&pid=ImgRaw&r=0'
            },
            {
           
           uuid: 'c70080cd-330f-4398-b169-03f057582e2a',
           name: 'Camera model 10', 
           description: 'Lorem ipsum dolor sit amet.', 
           price: 2550,
           photoURL: 'https://live.staticflickr.com/5595/15278680151_b3ecd9250f_b.jpg'
       },
       {
           
           uuid: 'c70080cd-330f-4398-b169-03f057582e2a',
           name: 'Camera model 11', 
           description: 'Lorem ipsum dolor sit amet.', 
           price: 2650,
           photoURL: 'https://live.staticflickr.com/65535/49690139461_55f0227ebc_b.jpg'
       },
       {
           
           uuid: 'c70080cd-330f-4398-b169-03f057582e2a',
           name: 'Camera model 12', 
           description: 'Lorem ipsum dolor sit amet.', 
           price: 1950,
           photoURL: 'https://c2.staticflickr.com/8/7304/11734414973_3f7a610389_b.jpg'
       },
       {
           
           uuid: 'c70080cd-330f-4398-b169-03f057582e2a',
           name: 'Camera model 13', 
           description: 'Lorem ipsum dolor sit amet.', 
           price: 1450,
           photoURL: 'https://www.35mmc.com/wp-content/uploads/2017/09/FBqSEEz-1080x720.jpg'
       },
       
       {
           
           uuid: 'c70080cd-330f-4398-b169-03f057582e2a',
           name: 'Camera model 14', 
           description: 'Lorem ipsum dolor sit amet.', 
           price: 2850,
           photoURL: 'https://i.etsystatic.com/7404966/r/il/9f7c99/1342040765/il_794xN.1342040765_6isx.jpg'
       },
       {
           
           uuid: 'c70080cd-330f-4398-b169-03f057582e2a',
           name: 'Camera model 15', 
           description: 'Lorem ipsum dolor sit amet.', 
           price: 2750,
           photoURL: 'https://live.staticflickr.com/3612/3586111196_7fef9478ce.jpg'
       }
       ]
           }
    },
    // method section
    methods: {
        addToCart(product) {
            let exists = false;
            
            for (const cartItem of this.shoppingCart) {
                if (cartItem.uuid === product.uuid) {
                    cartItem.amount = cartItem.amount + 1;
                    exists = true;
                    break;
                }
            }
            if (!exists) {
                this.shoppingCart.push({
                    ...product,
                    amount: 1,
                })
                  
            }
           
    },
  }
}
</script>
