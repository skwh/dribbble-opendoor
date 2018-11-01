<template>
  <main>
    <card title="1234 Example Rd." :action="{href:'#', text: 'view full offer'}">
      <table cellpadding="15px">
        <tr>
          <td>Home value</td>
          <td>$365,000</td>
        </tr>
        <tr>
          <td>
            Other closing costs
            <material-icon name="keyboard_arrow_down" size="24px"></material-icon>
          </td>
          <td>
            $2,000
          </td>
        </tr>
        <tr>
          <td>
            Estimated net proceeds
          </td>
          <td>
            <b>
              $346,000
            </b>
          </td>
        </tr>
      </table>
    </card>

    <card title="Next steps" action="">
      <checklist-timeline :items="items"></checklist-timeline>
      <button>
        <span>
          Next
        </span>
        Schedule your free assessment
      </button>
    </card>

    <card title="FAQs" :action="{href:'#', text: 'view all'}">
      <div v-for="(faq, index) in faqs"
           :key="`faq-${index}`"
           class="faq-item expandable">
        <material-icon name="keyboard_arrow_down" size="26px"></material-icon>
        <span>{{ faq }}</span>
      </div>
    </card>
  </main>
</template>

<script>
import ChecklistTimeline from './ChecklistTimeline.vue'

export default {
  name: 'OpendoorMainContent',
  components: { ChecklistTimeline },
  data () {
    return {
      faqs: [
        'Why is there a home condition assessment?',
        'What if repairs are needed on my home?',
        'How long does the selling process take?'
      ],
      items: [
        {
          completed: true,
          date: new Date(2018, 10, 15),
          primary_text: 'Setup and sign contract',
          secondary_text: 'Done'
        },
        {
          completed: false,
          date: new Date(2018, 10, 18),
          primary_text: 'Schedule your assessment',
          secondary_text: 'Schedule by 18 Nov'
        },
        {
          completed: false,
          date: new Date(2018, 10, 23),
          primary_text: 'Review or make repairs',
          secondary_text: 'Avaliable 2-3 days after'
        },
        {
          completed: false,
          date: new Date(2018, 10, 30),
          primary_text: 'Finalizing and closing',
          secondary_text: 'It\'s 15 days till we close'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
@import '../styles/variables';

main {
  grid-row-start: 3;
  grid-column-start: 4;

  table {
    width: 100%;

    tr {
      padding: 0.5rem;
    }

    td i {
      color: $blue;
      position: relative;
      top: 3px;
    }

    td:last-child {
      text-align: right;
    }
  }

  .faq-item {
    color: $grey;
    padding: 1rem 0.5rem;
    padding-left: 0;
    font-size: 0.9rem;

    i {
      color: $blue;
      position: relative;
      top: 3px;
      padding-right: 0.5rem;
    }
  }
}
</style>
