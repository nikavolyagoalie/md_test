1. Какой из двух фрагментов кода не сработает и почему?

Фрагмент 1:

	console.log( doubleNum(10) );

	let doubleNum = (num) => {
		let result = num * 2;
		return result;
	}

Фрагмент 2:

	console.log( doubleNum(10) );

	function doubleNum(num) {
    		let result = num * 2;
		return result;
	}

    Ответ: Фрагмент 1 - функциональное выражение Фрагмент 2 - объявление функции. Фрагмент 1 не сработает, потому что в функция вызывается раньше, чем она создается.


2. Исправьте ошибку в фрагменте коде так, чтобы после компиляции в шаблоне не было лишних тегов.

Ответ:
<template>
  <template v-for="i of count" :key="i">
    <component-name v-if="i < 10"/>
  </template>
</template>

<script>
import ComponentName from "./ComponentName.vue";

export default {
  components: {
    ComponentName,
  },
  data() {
    return {
      count: 20,
    };
  },
};
</script>

3. Есть массив некоторых строительных материалов, каждый элемент массива - объекты с ключами id и количества материала. Напишите функцию, которая будет возвращать oбьект в формате { "id":"count" }

Ответ:

newObjFormat(resources)

function newObjFormat(arr) {
    let obj = {}
    for (let item of arr) {
        obj[item.id] = item.count
    }
    return obj
}