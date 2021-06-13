<template>
  <div class="content">
    <n-card class="card">
      <n-form>
        <n-form-item>
          <n-input
            v-model:value="value"
            type="textarea"
            placeholder="请输入"
            :autosize="{ minRows: 2, maxRows: 5 }"
          />
        </n-form-item>
      </n-form>
    </n-card>
  </div>
</template>

<script lang="ts">
import { ref, defineComponent } from 'vue';
import { NInput, NCard, NFormItem, NForm } from 'naive-ui';
export default defineComponent({
  name: 'Demo',
  components: {
    NInput,
    NCard,
    NForm,
    NFormItem,
  },
  setup: () => {
    return {
      value: ref(''),
    };
  },
});
</script>

<style scoped>
.content {
  width: 100%;
  display: flex;
  justify-content: center;
}
.card {
  width: 30%;
}
</style>
