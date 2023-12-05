<template>
  <q-layout view="hHr lpr lfr">

    <q-header bordered style="height:6rem;border:none" class="bg-main text-white row items-center">
      <q-toolbar>
        <q-toolbar-title class="w100 row items-center justify-center">
          <div style="font-size:2.5rem;" class="text-grey-9 font-title q-pl-md">
            Sol Pratas
          </div>
        </q-toolbar-title>

        <q-btn dense flat round icon="menu" color="black" size="xl" @click="toggleRightDrawer" />
      </q-toolbar>
    </q-header>

    <q-drawer style="overflow-y:hidden" overlay v-model="rightDrawerOpen" side="right" bordered>
      <div class="w100" style="position:relative">
        <q-btn class="absolute-left q-mt-md q-ml-sm" dense flat round icon="close" color="red" size="md" @click="toggleRightDrawer" />
      </div>
        <div class="column items-center q-pt-sm justify-center bg-transparent">
            <div style="font-size:2rem" class="font-title  q-mb-md text-weight-bold low-opacity">M E N U</div>
            <span class="text-weight-bold font-satisfy text-white bg-grey-5 w100 text-center" style="font-size: 24px;">Sol Pratas</span>
            <!-- <div class="low-opacity w100" style="font-size: 12px;">{{ sessionData.role }}</div> -->
          <!-- <div class="low-opacity w100 text-center">@{{ sessionData.matricula }}</div> -->
        </div>
    <!-- items do menu -->
    <q-scroll-area style="height: 80vh; margin-top: 1rem; border-right: 1px solid #ddd">
      <q-list padding>
        <q-item clickable v-ripple to="/">
          <q-item-section avatar>
            <q-icon name="home" />
          </q-item-section>
          <q-item-section>
            Página Inicial
          </q-item-section>
        </q-item>
        <q-item clickable v-ripple to="/cadastrar">
          <q-item-section avatar>
            <q-icon name="library_add" />
          </q-item-section>

          <q-item-section>
            Cadastro de item
          </q-item-section>
        </q-item>
        <q-item clickable v-ripple to="/estoque">
          <q-item-section avatar>
            <q-icon name="inventory_2" />
          </q-item-section>
          <q-item-section>
            Estoque
          </q-item-section>
        </q-item>
        <!-- <q-item clickable v-ripple @click="logout()">
          <q-item-section avatar>
            <q-icon name="logout" />
          </q-item-section>

          <q-item-section>
            Fazer Logout
          </q-item-section>
        </q-item> -->

        <!-- <q-item clickable v-ripple class="absolute-bottom q-mb-sm" @click="verProjeto()"> -->
        </q-list>
    </q-scroll-area>
    </q-drawer>
    <q-page-container>
      <router-view />
    </q-page-container>

  </q-layout>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const rightDrawerOpen = ref(true)
function toggleRightDrawer () {
  rightDrawerOpen.value = !rightDrawerOpen.value
}

</script>
