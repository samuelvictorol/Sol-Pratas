<template>
    <div class="w100 ">
        <div class="w100 destaques q-py-md text-h4  low-opacity text-center q-mb-xs">Destaques</div>
        <div class="cards row no-wrap q-gutter-x-md q-mb-xl justify-center items-center">
            <div>
                <q-card class="my-card">
                    <q-parallax
                      src="https://www.elpatronplatas.com.br/cdn/shop/products/1_0802fc34-f026-4e07-9f2d-48071d40c2f6.jpg?v=1635356048"
                      :height="400"
                    />
                    <q-card-section>
                      <div class="text-h6">Corrente Prata 975</div>
                      <div class="text-subtitle2">R$ 149,90</div>
                      <div class="text-subtitle2 low-opacity"><s>R$ 199,90</s></div>
                      <q-btn icon-right="add_shopping_cart" class="q-my-md q-mr-md bg-green text-white absolute-right">Comprar <div class="q-pr-md"></div></q-btn>
                    </q-card-section>
                  </q-card>
            </div>
            <div>
                <q-card class="my-card">
                    <q-parallax
                      src="https://dh9mkiolokjyr.cloudfront.net/Custom/Content/Products/11/49/1149_brinco-prata-zirconia-redondo-10mm-pr-10909-f10mm_z2_637849440239659079.jpg"
                      :height="400"
                    />
                    <q-card-section>
                      <div class="text-h6">Brinco Prata 975</div>
                      <div class="text-subtitle2">R$ 89,90</div>
                      <div class="text-subtitle2 low-opacity"><s>R$ 99,90</s></div>
                      <q-btn icon-right="add_shopping_cart" class="q-my-md q-mr-md bg-green text-white absolute-right">Comprar <div class="q-pr-md"></div></q-btn>
                    </q-card-section>
                  </q-card>
            </div>
            <div>
                <q-card class="my-card">
                    <q-parallax
                      src="https://images.unsplash.com/photo-1573408301185-9146fe634ad0?q=80&w=2075&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                      :height="400"
                    />
                    <q-card-section>
                      <div class="text-h6">Pulseira Prata Exclusive</div>
                      <div class="text-subtitle2">R$ 49,90</div>
                      <div class="text-subtitle2 low-opacity"><s>R$ 89,90</s></div>
                      <q-btn icon-right="add_shopping_cart" class="q-my-md q-mr-md bg-green text-white absolute-right">Comprar <div class="q-pr-md"></div></q-btn>
                    </q-card-section>
                  </q-card>
            </div>
        </div>
    </div>
</template>
<script setup lang="ts">

</script>
<style scoped>
.my-card {
    width: 30rem;
    border: 4px double rgba(255, 255, 93, 0.478);
    border-radius: 12px;
}

@media (max-width:1200px) {
    .cards {
        display: flex;
        flex-direction: column;
        gap: 16px;
        margin-top: 1rem;
    }
    .my-card {
        width: 95vw;
    }
    .q-btn{
      position: relative;
    }
}

.destaques {
  background: #6190E8;   /* fallback for old browsers */
  background: -webkit-lin ear-gradient(to top, #FFFDE7, #fff);  /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to top, #FFFDE7, #fff); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  font-family: 'Montserrat Alternates', sans-serif;
}

</style>
