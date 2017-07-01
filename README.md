# vue-dataPicker
vue+datePicker.js 实现一个仿苹果手机的日历选择器

## 本人已经发布在npm上，可以直接输入

### 欢迎 Star or Issues
```
npm i --save vue-ios-datepicker
```

#### calendar.vue
```
<template>
  <div class="calendar">
    <p id="data">{{selectedData}}</p>
  </div>
</template>
import datePicker for 'vue-ios-daepicker'
export default {
  data () {
    return {
      selectedData: ''
    }
  },
  mounted () {
    let self = this
    let calendar = new dataPicker();
    calendar.init({
      'trigger': '#date', /*按钮选择器，用于触发弹出插件*/
      'type': 'date',/*模式：date日期；datetime日期时间；time时间；ym年月；*/
      'minDate':'2004-1-1',/*最小日期*/
      'maxDate':'2020-12-31',/*最大日期*/
      'onSubmit':function(){/*确认时触发事件*/
        self.selectedData = calendar.value
      },
      'onClose':function(){/*取消时触发事件*/
      }
    });
  }
}
```
