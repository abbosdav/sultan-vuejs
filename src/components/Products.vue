<template>
    <div class="product">
        <div class="product__container container">
            <div class="product__title title-products">
                Акционные <span>товары</span>
            </div>
            <div class="product__items">
                <article class="product__item item-product" v-for="product in products" :key="product.id">
                    <div class="item-product__labels">
                        <div class="item-product__label" v-for="(label,i) in product.labels" :key="i" :class="label.type">{{label.label}}</div>
                    </div>
                    <a href="" class="item-product__image ibg" :style="{backgroundImage:`url(${product.img})`}">
                        <!-- <img src=""/> -->
                    </a>
                    <div class="item-product__body">
                        <div class="item-product__size" :class="product.liquid ? 'icon-bottle' : 'icon-box'">
                            <span>{{product.size}}</span>
                        </div>
                        <div class="item-product__name"><span>{{product.brend}}</span>{{product.info}}</div>
                        <div class="item-product__params">
                            <div class="item-product__parametr">Штрихкод: <span>{{product.code}}</span></div>
                            <div class="item-product__parametr">Производитель: <span>{{product.plant}}</span></div>
                            <div class="item-product__parametr">Бренд: <span>{{product.brend}}</span></div>
                        </div>
                        <div class="item-product__btns">
                            <div class="item-product__price">{{product.price}}</div>
                            <button class="item-product__button">В КОРЗИНУ<span class="icon-cart"></span></button>
                        </div>
                    </div>
                </article>
                
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return{
            products: [
                {
                    id:1,
                    img: require('@/assets/img/product1.png'),
                    size: '450 мл',
                    labels: [
                        
                        {
                            type:'popular',
                            label:'ПОПУЛЯРНОЕ'
                        }
                    ],
                    liquid: true,
                    brend: 'AOS',
                    info: 'Ср-во для мытья посуды Апельсин+мята',
                    code: '4604049097548',
                    plant: 'Нэфис',
                    price: '48,76 ₸'
                },
                {
                    id:2,
                    img: require('@/assets/img/product1.png'),
                    size: '450 мл',
                    labels: [
                        {
                            type:'best',
                            label: 'ЛУЧШИЙ ВЫБОР'
                        }
                    ],
                    liquid: true,
                    brend: 'AOS',
                    info: 'Ср-во для мытья посуды Апельсин+мята',
                    code: '4604049097548',
                    plant: 'Нэфис',
                    price: '48,76 ₸'
                },
                {
                    id:1,
                    img: require('@/assets/img/product3.jpg'),
                    size: '450 мл',
                    labels: [
                        {
                            type:'new',
                            label:'НОВИНКА'
                        }
                    ],
                    liquid: false,
                    brend: 'AOS',
                    info: 'Ср-во для мытья посуды Апельсин+мята',
                    code: '4604049097548',
                    plant: 'Нэфис',
                    price: '48,76 ₸'
                },
                {
                    id:1,
                    img: require('@/assets/img/product1.png'),
                    size: '450 мл',
                    labels: [
                        {
                            type:'new',
                            label:'НОВИНКА'
                        },
                        {
                            type:'sale',
                            label:'СКИДКА'
                        }
                    ],
                    liquid:true,
                    brend: 'AOS',
                    info: 'Ср-во для мытья посуды Апельсин+мята',
                    code: '4604049097548',
                    plant: 'Нэфис',
                    price: '48,76 ₸'
                },
                {
                    id:1,
                    img: require('@/assets/img/product1.png'),
                    size: '450 мл',
                    labels: [
                        
                        {
                            type:'popular',
                            label:'ПОПУЛЯРНОЕ'
                        }
                    ],
                    liquid: true,
                    brend: 'AOS',
                    info: 'Ср-во для мытья посуды Апельсин+мята',
                    code: '4604049097548',
                    plant: 'Нэфис',
                    price: '48,76 ₸'
                },
                {
                    id:2,
                    img: require('@/assets/img/product1.png'),
                    size: '450 мл',
                    labels: [
                        {
                            type:'best',
                            label: 'ЛУЧШИЙ ВЫБОР'
                        }
                    ],
                    liquid: true,
                    brend: 'AOS',
                    info: 'Ср-во для мытья посуды Апельсин+мята',
                    code: '4604049097548',
                    plant: 'Нэфис',
                    price: '48,76 ₸'
                },
                {
                    id:1,
                    img: require('@/assets/img/product3.jpg'),
                    size: '450 мл',
                    labels: [
                        {
                            type:'new',
                            label:'НОВИНКА'
                        }
                    ],
                    liquid: false,
                    brend: 'AOS',
                    info: 'Ср-во для мытья посуды Апельсин+мята',
                    code: '4604049097548',
                    plant: 'Нэфис',
                    price: '48,76 ₸'
                },
                {
                    id:1,
                    img: require('@/assets/img/product1.png'),
                    size: '450 мл',
                    labels: [
                        {
                            type:'new',
                            label:'НОВИНКА'
                        },
                        {
                            type:'sale',
                            label:'СКИДКА'
                        }
                    ],
                    liquid:true,
                    brend: 'AOS',
                    info: 'Ср-во для мытья посуды Апельсин+мята',
                    code: '4604049097548',
                    plant: 'Нэфис',
                    price: '48,76 ₸'
                },
            ],
            productTitle: 'Акционные товары'
        }
    },
    methods:{
    
    }
}
</script>
<style lang="scss" scoped>
.product {

		// .product__container

		&__container {
		}

		// .product__title

		&__title {
            margin-top: 100px;
            color: #FFC85E;
            font-size: 40px;
            font-family: 'i-bold';
            & span{
                color: #000;
                font-size: 40px;
            }
		}

		// .product__items

		&__items {
            margin-bottom: 100px;
            margin-top: 50px;
            display: grid;
            gap: 21px;
            grid-template-columns: repeat(auto-fit, minmax(318px, 2fr));
		}

		// .product__item

		&__item {
            padding: 15px;
            box-shadow: 0px 14px 39px -11px rgba(0, 0, 0, 0.06);
            border-radius: 10px;
            position: relative;
		}
}
.container {
}
.title-products {
}
.item-product {

		// .item-product__labels

		&__labels {
            position: absolute;
            top: 29px;
		}

		// .item-product__label

		&__label {
            border-radius: 5px;
            text-align: center;
            padding: 5px 10px;
            color: #fff;
            margin-bottom: 5px;
            &.popular{
                background-color: #1FD85D;
            }
            &.sale{
                background-color: #D81F1F;
            }
            &.new{
                background-color: #6DAEEA;
            }
            &.best{
                background-color: #1FD8CD;
            }
            &.cash{
                background-color: #D06EFE;
            }
		}

		// .item-product__image

		&__image {
            width: 100%;
            min-height: 192px;
            display: block;
            background-repeat: no-repeat;
            // background-size: cover;
            background-position: center;
            margin-top: 42px;
            
		}

		// .item-product__body

		&__body {
            margin-left: 8px;
		}

		// .item-product__size

		&__size {
            color: #3F4E65;
            margin-bottom: 10px;
            & span{
                color: #3F4E65;
                margin-left: 8px;
            }
		}

		// .item-product__name

		&__name {
            font-size: 16px;
            width: 315px;
            font-weight: 800;
            line-height: 20/16*100%;
            margin-bottom: 20px;
            & span{
                font-family: 'i-bold';
                margin-right: 5px;
            }
		}

		// .item-product__params

		&__params {
            margin-bottom: 15px;
		}

		// .item-product__parametr

		&__parametr {
            font-size: 14px;
            color: #3F4E65;
            font-weight: 300;
            & span{
                font-family: 'i-bold';
                font-weight: 500;
                color: #000;
            }
            &:not(:last-child){
                margin-bottom: 5px;
            }
		}
        // item-product__btns
        &__btns{
            display: flex;
            align-items: center;
        }
        &__price{
            font-family: 'i-bold';
            font-weight: 800;
        }
        &__button{
            min-width: 153px;
            color: #fff;
            background-color: #FFC85E;
            border: unset;
            padding: 15px 25px;
            border-radius: 79px;
            margin:0 0 14px 40px;
            transition: background-color 0.5s ease 0s;
            @media (any-hover:hover) {
                    &:hover{
                        background-color: #e4a72e;
                    }
            }        
            & span{
                margin-left: 5px;
            }
        }
}
.new {
}
.ibg {
}
.icon-bottle {
    &::before{
        color: #3F4E65;
        font-size: 15px;
    }
}

</style>
