﻿<template>
    <div class="header boxShadow">
        <b-row class="mktPlace" align-v="start">
            <b-col cols="6" md="6">
                <h6 @click.prevent="goProducts()" class="alterCursor"><b class="mktColor">Mkt</b><b class="placeColor">Place</b></h6>
            </b-col>
            <b-col cols="6" md="6">
                <p @click.prevent="goShoppingCart()" class="alignProduct alterCursor textConfig">
                    Produtos &nbsp;&nbsp;
                    <img @click.prevent="goRequests()" class="img alterCursor" src="@/assets/icons/shopping-cart.svg" />
                </p>
            </b-col>
        </b-row>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                products: {}
            };
        },
        methods: {
            goProducts() {
                this.$router.push({ path: "/products" }).catch(err => { });
            },
            goShoppingCart() {
                this.$router.push({ path: "/shoppingcart" }).catch(err => { });
            },
        },
    };
</script>

<style scoped>
    .header {
        z-index: 1;
        top: 0;
        position: fixed;
        width: 100%;
        text-align: center;
        background-color: white;
        padding: 10px;
    }

    .mktPlace {
        padding-left: 10px
    }

    .mktColor {
        color: dimgray;
    }

    .placeColor {
        color: blueviolet;
    }

    .img {
        max-width: 150px;
    }

    .alignProduct {
        margin-right: 10%;
    }

    .alterCursor {
        cursor: pointer;
    }

    .textConfig {
        font-size: 12px;
    }

    .boxShadow {
        box-shadow: 0px 1px 5px lightgrey;
    }
</style>