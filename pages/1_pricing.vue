<template>
    <v-container>
        <v-col>
            <v-col align="center">
                <PricingSelect v-on:setType="setType"/>
                <h1>Pricing</h1>
            </v-col>
            <div style="display: grid; grid-template-columns: repeat(3,1f); gap: 32px; margin-top: 80px auto 40px; margin-top: 20px">
                <PricingCard v-bind:data="data[type][0]" />
                <PricingCard v-bind:data="data[type][1]" />
                <PricingCard v-bind:data="data[type][2]" />
            </div>
        </v-col>
    </v-container>
</template>