<template>
  <div class="container">
    <h3>Test</h3>
    <ol>
      <li>
        Find the missing numbers from 1 to 100<br />
        Answer:
        <strong v-for="(number, idx) in answer_6b" :key="idx">
          {{ `${number}` }}{{ idx != answer_6b.length ? ", " : "" }}</strong
        >
      </li>
      <li>
        return the number which is called more than 1<br />
        Answer:
        <strong v-for="(number, idx) in answer_6c" :key="idx">
          {{ `${number}` }}{{ idx != answer_6c.length ? ", " : "" }}</strong
        >
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  data() {
    return {
      numbers_6b: [
        1,
        2,
        4,
        5,
        6,
        7,
        8,
        10,
        11,
        12,
        13,
        14,
        15,
        16,
        17,
        18,
        19,
        20,
        21,
        22,
        23,
        24,
        25,
        26,
        27,
        28,
        29,
        30,
        31,
        32,
        33,
        34,
        35,
        36,
        37,
        38,
        39,
        40,
        42,
        43,
        44,
        45,
        46,
        47,
        48,
        49,
        50,
        51,
        52,
        53,
        54,
        55,
        56,
        57,
        58,
        59,
        61,
        62,
        63,
        64,
        65,
        66,
        67,
        68,
        69,
        70,
        72,
        73,
        74,
        75,
        76,
        77,
        78,
        79,
        80,
        81,
        82,
        83,
        84,
        85,
        86,
        87,
        88,
        89,
        90,
        91,
        92,
        93,
        94,
        95,
        96,
        97,
        98,
        99,
        100,
      ],
      numbers_6c: [
        1,
        2,
        3,
        4,
        5,
        6,
        7,
        8,
        9,
        10,
        11,
        12,
        13,
        14,
        15,
        16,
        17,
        18,
        19,
        20,
        21,
        22,
        23,
        24,
        25,
        25,
        25,
        25,
        25,
        26,
        27,
        28,
        29,
        30,
        31,
        32,
        33,
        34,
        34,
        34,
        34,
        35,
        36,
        37,
        38,
        39,
        40,
        41,
        42,
        43,
        44,
        45,
        46,
        47,
        48,
        49,
        50,
        51,
        52,
        53,
        54,
        55,
        56,
        57,
        58,
        59,
        60,
        61,
        62,
        62,
        63,
        64,
        65,
        66,
        67,
        68,
        69,
        70,
        71,
        72,
        73,
        74,
        75,
        76,
        77,
        78,
        79,
        80,
        81,
        82,
        83,
        83,
        83,
        84,
        85,
        86,
        87,
        88,
        89,
        90,
        91,
        92,
        92,
        93,
        94,
        95,
        96,
        97,
        98,
        99,
        100,
      ],
      array_code: [
        "1.",
        "1.1.",
        "1.2.",
        "1.3.",
        "1.4.",
        "1.1.1.",
        "1.1.2.",
        "1.1.3.",
        "1.2.1.",
        "1.2.2.",
        "1.3.1.",
        "1.3.2.",
        "1.3.3.",
        "1.3.4.",
        "1.4.1.",
        "1.4.3.",
      ],
      answer_6b: [],
      answer_6c: [],
      answer_6d: {},
    };
  },

  methods: {
    getAnswer6B() {
      // 6. B. Find the missing numbers from 1 to 100
      let i = 0;
      let j = 0;
      while (i < 100) {
        if (i + 1 != this.numbers_6b[j]) {
          this.answer_6b.push(i + 1);
        } else {
          j++;
        }
        i++;
      }
    },

    getAnswer6C() {
      // 6. C. return the number which is called more than 1
      let max = Math.max(...this.numbers_6c);
      let numbers = new Array(max + 1).fill(0);
      this.numbers_6c.map((e) => {
        numbers[e] += 1;
      });
      numbers.map((e, idx) => {
        if (e > 1) this.answer_6c.push(idx);
      });
    },
    getAnswer6D() {},
  },
  mounted() {
    this.getAnswer6B();
    this.getAnswer6C();
    this.getAnswer6D();
  },
};
</script>

<style lang="scss" scoped></style>
