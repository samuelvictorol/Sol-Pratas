<template>
  <q-layout view="hHh lpR lfr">

    <q-header bordered style="height:6rem" class="bg-main text-white row items-center">
      <q-toolbar>
        <q-toolbar-title class="w100 row items-center justify-center">
          <div style="font-size:2.5rem" class="font-title q-pl-md">
            Sol Pratas
          </div>
        </q-toolbar-title>

        <q-btn dense flat round icon="menu" @click="toggleRightDrawer" />
      </q-toolbar>
    </q-header>

    <q-drawer show-if-above v-model="rightDrawerOpen" side="right" bordered>

        <div class="row items-center justify-center bg-transparent">
            <div style="font-size:2rem" class="font-title q-pt-xl text-weight-bold">Sol Pratas</div>
            <!-- <div class="low-opacity w100" style="font-size: 12px;">{{ sessionData.role }}</div> -->
          <!-- <div class="low-opacity w100 text-center">@{{ sessionData.matricula }}</div> -->
        </div>
    <!-- items do menu -->
    <q-scroll-area style="height: calc(100% - 5rem); margin-top: 2rem; border-right: 1px solid #ddd">
      <q-list padding>
        <q-item clickable v-ripple to="/">
          <q-item-section avatar>
            <q-icon name="inventory_2" />
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
        <q-item clickable v-ripple class="absolute-bottom q-mb-sm">
          <q-item-section avatar>
          </q-item-section>
          <q-item-section class="low-opacity q-pl-xl">
            Sol Pratas
          </q-item-section>
        </q-item>
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
