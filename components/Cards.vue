<script setup lang="ts">
import CardWithProps from "../components/CardWithProps.vue";
import CardWithSlot from "../components/CardWithSlot.vue";
</script>

<template>
  <section>
    <h1>カードコンポーネントの例</h1>
    <h2>スロットを使った例</h2>
    <div :class="styles.wrapper">
      <CardWithSlot>
        <template #header>
          <h3>まりえってぃさん</h3>
        </template>
        <template #body>
          <img :src="'https://ca.slack-edge.com/TF8E0DCGN-U027AU766LT-7a809b9f3989-512'" width="200" height="200" />
        </template>
        <template #footer>
          <p>PD室の太陽です。彼女がいるおかげでPD室が明るくなっています。</p>
        </template>
      </CardWithSlot>
      <CardWithSlot>
        <template #header>
          <h3>こみーさん</h3>
        </template>
        <template #body>
          <img :src="'https://ca.slack-edge.com/TF8E0DCGN-UL01QC2MT-416b2aa60407-512'" width="200" height="200" />
        </template>
        <template #footer>
          <p>MCSの守護神です。彼がいなければMSCの開発組織は成り立ちません。</p>
        </template>
      </CardWithSlot>
    </div>
  </section>
  <section>
    <h2>Propsを使った例</h2>
    <div :class="styles.wrapper">
      <CardWithProps
        title="まりえってぃさん"
        imageUrl="https://ca.slack-edge.com/TF8E0DCGN-U027AU766LT-7a809b9f3989-512"
        description="PD室の太陽です。彼女がいるおかげでPD室が明るくなっています。"
      />
      <CardWithProps
        title="こみーさん"
        imageUrl="https://ca.slack-edge.com/TF8E0DCGN-UL01QC2MT-416b2aa60407-512"
        description="MCSの守護神です。彼がいなければMSCの開発組織は成り立たない。"
      />
    </div>
  </section>
</template>

<style module="styles">
.wrapper {
  display: flex;
  gap: 16px;
}
</style>
