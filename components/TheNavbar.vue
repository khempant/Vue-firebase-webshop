<template>
    <div>
        <nav class="navbar navbar-expand-lg navbar-dark bg-dark mb-3">
            <div class="container-fluid">
                <NuxtLink to="/" class="navbar-brand">
                    Camera Shop
                </NuxtLink>
                
                
                <button type="button" class="btn btn-primary">Login</button>
                        <button type="button" class="btn btn-secondary">Register</button>
                <div class="collapse navbar-collapse" id="navbarSupportedContent">
                    <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                        
                    </ul>
                    <div class="d-flex">
                        <button
                        class="btn btn-outline-primary"
                        type="button"
                        data-bs-toggle="offcanvas"
                        data-bs-target="#offcanvasRight"
                        aria-controls="offcanvasRight"
                        >
                    Shopping cart
                </button>
                    </div>
                </div>
            </div>
        </nav>
    </div>
</template>