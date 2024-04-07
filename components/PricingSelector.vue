<template>
  <div role="tablist" aria-label="Select a product" class="pricing-selector">
    <div :class="{active:type == 0}" class="item noactive" @click="onClick(0)">
        <p><strong>Figma</strong></p>
    </div>        
        <div :class="{active:type == 1}" class="item noactive" @click="onClick(1)">
            <p><strong>FigJam</strong></p>
        </div>
    </div>        
</template>

<script>
    export default {
        data() {
           return {
                 type: 0,
            } 
        },
        methods:{
            onClick(type) {
                this.type = type;
                this.$emit('selectType', this.type);
            },
        }
    }
</script>

<style scoped>
.pricing-selector {
  border-radius: 8px;
  border: 2px solid rgb(229, 229, 229);
  background: rgb(255, 255, 255);
  display: inline-flex;
  padding: 4px;
  gap: 3px;
}

.item {
    font-size: 1.25rem;
    background: rgb(255, 255, 255);
    color: black;
    padding: 12px 32px;
    text-align: center;
    border-radius: 8px;
}

.active {
    background: rgb(85, 81, 255);
    color: white;
}
</style>
