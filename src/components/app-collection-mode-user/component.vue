<template>
  <app-collection-body
    type="image, list-item, actions"
    :height="313"
    :loading="loading">
    <app-collection-cover class="pa-2 pb-0" :value="icons" :id="id" :illustration="illustration"/>
    <app-collection-text class="pb-0" justify>
      <app-collection-info-name :value="name" class="mr-2"/>
      <app-collection-info-count-icons :value="countIcons"/>
    </app-collection-text>
    <app-collection-text justify>
      <app-collection-info-time :value="timeUpdate"/>
      <app-collection-info-count-visits :value="countVisits"/>
    </app-collection-text>
    <app-collection-action-group>
      <app-collection-action-item-likes :id="id" :value="countLikes"/>
    </app-collection-action-group>
  </app-collection-body>
</template>

<script>
import mixinComponentCollection from '@/mixins/component-collection.js'

export default {
  name: 'app-collection-mode-user',
  mixins: [
    mixinComponentCollection
  ]
}
</script>
