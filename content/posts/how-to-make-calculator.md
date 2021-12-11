---
title: How to make calculator
author: "Silver Jõemetsa"
---

It's so easy! Writing a simple calculator is a lot of fun.

Here's what we're going to build today:

<Calculator></Calculator>

<br />

So let's get started!

<br />

## First define the template
```vue
<template>
  <div class="calculator">
    <div class="calculator__display">
      <span class="calculator__display-value">{{ displayValue }}</span>
    </div>

    <div class="calculator__buttons">
      <button v-for="(button, index) in buttons" :key="index" class="calculator__button" @click="handleClick(button)">
        {{ button }}
      </button>
    </div>
  </div>
</template>

```

As you can see, we use `BEM` naming convention for the components.

## Then defined the data and methods
```vue
<script>
export default {
  data () {
    return {
      displayValue: '0',
      buttons: [
        'AC',
        '+/-',
        '%',
        '/',
        '7',
        '8',
        '9',
        '*',
        '4',
        '5',
        '6',
        '-',
        '1',
        '2',
        '3',
        '+',
        '0',
        '.',
        '='
      ]
    }
  },
  methods: {
    handleClick (button) {
      if (button === 'AC') {
        this.displayValue = '0'
      } else if (button === '+/-') {
        this.displayValue = this.displayValue * -1
      } else if (button === '%') {
        this.displayValue = this.displayValue / 100
      } else if (button === '+' || button === '-' || button === '*' || button === '/') {
        this.displayValue = this.displayValue + button
      } else if (button === '=') {
        // eslint-disable-next-line no-eval
        this.displayValue = eval(this.displayValue)
      } else {
        if (this.displayValue === '0') {
          this.displayValue = ''
        }
        this.displayValue += button
      }
    }
  }
}
</script>
```

## And finally the styles
```vue
<style lang="scss" scoped>
.calculator {
  width: 200px;
}

.calculator__display {
  background: #eee;
  padding: 10px;
}

.calculator__buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
}

.calculator__button {
  display: block;
}
</style>

```
