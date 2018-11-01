<template>
  <div class="checklist-timeline">
    <div v-for="(item, index) in items"
         :key="`checkmarkItem-${index}`"
         class="checklist-item">
      <checkmark :checked="item.completed"></checkmark>
      <div class="date">
        <span class="month">{{ convertMonth(item.date.getMonth()) }}</span>
        <span class="day">{{ item.date.getDate() }}</span>
      </div>
      <div class="text">
        <h5>{{ item.primary_text }}</h5>
        <p>{{ item.secondary_text }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ChecklistTimeline',
  props: ['items'],
  /*
    Items is an array of checklist timeline items
    Each item has the following structure:
    {
      completed: boolean
      date: date
      primary_text: string
      secondary_text: string
    }
  */
  methods: {
    convertMonth (monthNumber) {
      return 'Nov'
    }
  }
}
</script>

<style scoped lang="scss">

</style>
