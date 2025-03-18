<script setup lang="ts">
const props = defineProps<{
  name: string;
  image: string;
  altText?: string;
  minetip: string;
  rarity?: string;
  durability?: string;
  renewable?: string;
  stackable?: string;
}>();
</script>

<template>
  <div class="item-details-table">
    <div class="item-details-table-header">
      {{ props.name }}
    </div>
    <div class="infobox-imagearea animated-container">
      <div>
        <span class="pixel-image" typeof="mw:File"
          ><a :href="props.image" class="mw-file-description" title=""
            ><img
              :alt="props.altText"
              :src="props.image"
              decoding="async"
              loading="lazy"
              width="160"
              height="160"
              class="mw-file-element"
              data-file-width="160"
              data-file-height="160" /></a
        ></span>
      </div>
      <div class="infobox-invimages">
        <div>
          <span class="invslot"
            ><span class="invslot-item invslot-item-image" :data-minetip-title="props.minetip"
              ><span typeof="mw:File"
                ><span
                  ><img
                    :alt="props.altText"
                    :src="props.image"
                    decoding="async"
                    loading="lazy"
                    width="32"
                    height="32"
                    class="mw-file-element"
                    data-file-width="32"
                    data-file-height="32" /></span></span></span
          ></span>
        </div>
      </div>
    </div>
    <table cellspacing="1" cellpadding="4">
      <tbody>
        <tr v-if="!!props.rarity">
          <th title="The rarity tier of this item.">Rarity tier:</th>
          <td>
            {{ props.rarity }}
          </td>
        </tr>
        <tr v-if="!!props.durability">
          <th title="The maximum durability of this item.">Durability:</th>
          <td>
            {{ props.durability }}
          </td>
        </tr>
        <tr v-if="!!props.renewable">
          <th title="Whether or not the item is renewable.">Renewable:</th>
          <td>
            {{ props.renewable }}
          </td>
        </tr>
        <tr v-if="!!props.stackable">
          <th title="Whether or not the item is stackable.">Stackable:</th>
          <td>
            {{ props.stackable }}
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<style lang="scss">
.item-details-table {
  border: 1px solid #0e6a3b !important;
  position: relative;
  clear: right;
  margin: 0 0 1em 1em;
  width: 306px;
  font-size: 90%;
  background: var(--light-bg-color);
  float: right;
  padding: 2px;
  overflow: auto;
  & > table {
    font-size: 12.6px;
    margin: 0;
    width: 100%;
    border: none;
    border-radius: 0px;
    display: table;
    & > tbody {
      border-top: var(--border);
    }
  }
  & > .item-details-table-header {
    font-size: 120%;
    padding: 5px;
    font-weight: bold;
    text-shadow: 2px 2px 0 #084023;
    margin: 1px 2px 0;
    background-color: #0e6a3b;
    border-inline: 3px solid #075032 !important;
    border-top: 3px solid #328058 !important;
    border-bottom: 3px solid #084023 !important;
    text-align: center;
    & > code {
      text-shadow: none;
    }
  }
  & > tr,
  td,
  th {
    border: none;
    text-align: left !important;
  }
}
@media (max-width: 600px) {
  .item-details-table {
    width: auto;
    margin-left: 0;
    float: none;
  }
}
</style>
