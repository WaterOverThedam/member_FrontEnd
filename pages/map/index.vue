<template>
  <div>
    <group title="vux demo">
      <cell title="cell" value="click me" is-link @click.native="alert"></cell>
      <Datetime title='birthday'></Datetime>
      <Calendar title='birthday'></Calendar>
     <vue-datepicker-local v-model="range"></vue-datepicker-local>
    </group>

 
  </div>
</template>


<script>
import VueDatepickerLocal from '~/components/VueDatepickerLocal'
import { Datetime,Calendar} from 'vux'
 
export default {
  data() {
    return {
      title: 'vux demo',
      time: new Date(),
      range: [new Date(),new Date()],
      emptyTime: '',
      emptyRange: [],
      local: {
        dow: 0, // Sunday is the first day of the week
        hourTip: 'Select Hour', // tip of select hour
        minuteTip: 'Select Minute', // tip of select minute
        secondTip: 'Select Second', // tip of select second
        yearSuffix: '', // suffix of head year
        monthsHead: 'January_February_March_April_May_June_July_August_September_October_November_December'.split('_'), // 
        months: 'Jan_Feb_Mar_Apr_May_Jun_Jul_Aug_Sep_Oct_Nov_Dec'.split('_'), // months of panel
        weeks: 'Su_Mo_Tu_We_Th_Fr_Sa'.split('_'), // weeks,
        cancelTip: 'cancel',
        submitTip: 'confirm'
      }
    }
  },
  components: {
    Datetime,
    Calendar,
    VueDatepickerLocal 
  },
  methods: {
    alert() {
      this.$vux.alert.show('This is a Alert example.')
    }
  }
}
</script>

 