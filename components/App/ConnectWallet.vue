<script setup lang="ts">
import { getAddresses } from "@/app/services/wallet";
import { getInjectiveAddress } from "@injectivelabs/sdk-ts";

const address = ref("");

function handleConnectWallet() {
  if (address.value) {
    address.value = "";
    return;
  }
  getAddresses().then(
    ([ethAddress]) => (address.value = getInjectiveAddress(ethAddress))
  );
}
</script>

<template>
  <AppButton @click="handleConnectWallet">{{
    address ? `${address.slice(0, 4)}...${address.slice(-5)}` : "Connect Wallet"
  }}</AppButton>
</template>
