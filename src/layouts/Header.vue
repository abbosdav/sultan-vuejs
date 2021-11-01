<template>
    <div class="wrapper">
        <div class="header__body">
            <div class="header__top">
                <div class="header__container container">
                    <div class="header__address address-header">
                        <div class="address-header__place">
                            <div class="address-header__location icon-location"></div>
                            <a href="" class="address-header__content">
                                <div class="address-header__title">г. Кокчетав, ул. Ж. Ташенова 129Б</div>
                                <div class="address-header__text">(Рынок Восточный)</div>
                            </a>
                        </div>
                        <div class="address-header__place">
                            <div class="address-header__location icon-massage"></div>
                            <a href="" class="address-header__content">
                                <div class="address-header__title">opt.sultan@mail.ru</div>
                                <div class="address-header__text">На связи в любое время</div>
                            </a>
                        </div>
                    </div>
                    <div class="header__menu menu-header">
                        <ul class="menu-header__list">
                            <li class="menu-header__item">
                                <a href="" class="menu-header__link">О компании</a>
                            </li>
                            <li class="menu-header__item">
                                <a href="" class="menu-header__link">Доставка и оплата</a>
                            </li>
                            <li class="menu-header__item">
                                <a href="" class="menu-header__link">Возврат</a>
                            </li>
                            <li class="menu-header__item">
                                <a href="" class="menu-header__link">Контакты</a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
            <div class="header__bottom">
                <div class="header__container container">
                    <div class="header__logo">
                    <img src="@/assets/img/logo.png" alt="">
                </div>
                <a href="" class="header__btn btn-header">
                    <span class="btn-header__title">Каталог</span>
                    <div class="btn-header__boxes">
                        <span></span>
                        <span></span>
                    </div>
                </a>
                <div class="header__search search-header">
                    <button type="button" class="search-header__btn icon-search">Поиск</button>
                    <form action="" class="search-header__form">
                        <input type="search" placeholder="Поиск...">
                        <button type="submit" class="icon-search"></button>
                    </form>
                </div>
                <div class="header__connect connect-header">
                    <div class="connect-header__content">
                        <div class="connect-header__phone">+7 (777) 490-00-91</div>
                        <div class="connect-header__data">время работы: 9:00-20:00</div>
                        <a href="" class="connect-header__btn">Заказать звонок</a>
                    </div>
                    <div class="connect-header__img">
                        <img src="@/assets/img/dispet.png" alt="">
                        <span class="connect-header__indicator"></span>
                    </div>
                </div>
                <a href="" class="header__btn btn-header">
                    <span class="btn-header__title">Прайс-лист</span>
                    <div class="btn-header__load icon-download"></div>
                </a>
                <div class="header__cart cart-header">
                    <div class="cart-header__icon icon-cart">
                        <span class="cart-header__count">2</span>
                    </div>
                    <div class="cart-header__content">
                        <div class="cart-header__title">Корзина</div>
                        <div class="cart-header__general">12 478 ₸ </div>
                    </div>
                </div>
                </div>
                
            </div>
        </div>
    </div>
</template>
<style lang="scss">
    .header {

        // .header__container

        &__container {
           
        }

        // .header__body

        &__body {
        }

        // .header__top

        &__top {
            display: flex;
            justify-content: space-between;
            padding: 14px 0px;
        }

        // .header__address

        &__address {
            flex: 0 0 476px;
            display: flex;
            justify-content: space-between;
        }

        // .header__menu

        &__menu {
        }

        // .header__bottom

        &__bottom {
        }
    }

.address-header {

		// .address-header__place

		&__place {
            display: flex;
            align-items: center;
		}
        // .address-header__location
        &__location{
            margin-right: 18px;
        }
        // .address-header__content
        &__content{
            color: #000;
            transition: color 0.3s ease 0s ;
            @media (any-hover: hover) {
                &:hover{
                    color: #eca414;
                }
            }
        }

		// .address-header__title

		&__title {
            font-size: 12px;
            font-family: 'i-bold';
		}

		// .address-header__text

		&__text {
            font-size: 12px;
            font-family: 'i-regular';
		}

		// .address-header__email

		&__email {
        
		}
}
.icon-location {
    &::before{
        font-size: 14px;
    }
}
.icon-massage {
    &::before{
        font-size: 14px;
    }
}
.menu-header {
    flex: 0 1 auto;

    // .menu-header__list

    &__list {
        display: flex;
    }

    // .menu-header__item

    &__item {
        &:not(:last-child){
            padding-right: 30px;
        }
    }

    // .menu-header__link

    &__link {
        color: #000;
        font-size: 14px;
        font-family: 'i-regular';
        transition: color 0.3s ease 0s;
        @media (any-hover: hover) {
            &:hover{
                color: #eca414;
            }
            
        }
    }
}

// header-bottom----------------------
.search-header__btn{
    display: none;
}
.header {
		// .header__bottom
        &__bottom{
            border-top: 1px solid #3F4E65;
        }

		&__container {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
		}

		// .header__logo

		&__logo {
            & img{
                max-width: 156px;
            }
		}

		// .header__btn

		&__btn {
            padding: 21px 54px;
            background-color: #FFC85E;
            color: #fff;
            border-radius: 79px;
		}

		// .header__search

		&__search {
		}

		// .header__connect

		&__connect {
		}

		// .header__cart

		&__cart {
		}
}
.btn-header {
    display: flex;
    align-items: center;

    &__title{
    
    }

		// .btn-header__title

		&__boxes {
            margin-left: 5px;
            & span{
                width: 7px;
                height: 7px;
                display: block;
                border: 1px solid #fff;
                position: relative;
                &:not(:last-child){
                    margin-bottom: 1px;
                }
                &::after{
                    content: '';
                    width: 5px;
                    height: 5px;
                    top: -1px;
                    left: 7px;
                    border: solid 1px #fff;
                    position: absolute;
                }
            }
		}
}
.search-header {
    background-color: #EDEDED;
    padding: 10px 10px 10px 20px;
    border-radius: 79px;
    &__form{
        align-items: center;
        & input{
            background-color: transparent;
            border: inherit;
            &:focus{
                outline: none;
            }
        }
        & button{
            background-color: #FFC85E;
            color: #fff;
            padding: 13px;
            border-radius: 50%;
            border: unset;
        }

    }
		// .search-header__btn
    &__btn {
    }
}
.icon-search {
}
.connect-header {
    display: flex;
    align-items: center;
		// .connect-header__content

		&__content {
            margin-right: 10px;
            text-align: right;
		}

		// .connect-header__phone

		&__phone {
            font-size: 14px;
            color: #000;
            font-family: 'i-bold';
            line-height: 18/14*100%;
            margin-bottom: 5px;
		}

		// .connect-header__data

		&__data {
            font-size: 12px;
            color: #000;
            line-height: 18/12*100%;

		}

		// .connect-header__btn

		&__btn {
            font-size: 10px;
            line-height: 150%;
            color: #000;
            transition: text-decoration 0.3s ease 0s;
            @media (any-hover:hover) {
                &:hover{
                    color: rgb(31, 27, 137);
                    text-decoration: underline;
                }
                
            }
		}

		// .connect-header__img

		&__img {
            position: relative;
            & img{
                height: 113px;
                border-radius: 50%;
            }
		}
        &__indicator{
            width: 8px;
            height: 8px;
            background: #1FD85D;
            border-radius: 50%;
            position: absolute;
            top: 35px;
            right: 0px;
        }
}
.btn-header{
    &__load{
        margin-left: 15px;
    }
}
.icon-download {
}
.cart-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex: 0 1 128px;

		// .cart-header__icon

		&__icon {
            position: relative;
            font-size: 30px;
		}

		// .cart-header__count

		&__count {
            display: inline-block;
            width: 17px;
            height: 17px;
            text-align: center;
            align-items: center;
            position: absolute;
            right: -8px;
            top: -5px;
            padding: 3px;
            color: #fff;
            border-radius: 50%;
            background: #FFC85E;
            font-size: 12px;
		}

		// .cart-header__content

		&__content {
		}

		// .cart-header__title

		&__title {
            font-size: 12px;
            line-height: 18/12*100%;
		}

		// .cart-header__general

		&__general {
            font-size: 14px;
            line-height: 18/12*100%;
            font-family: 'i-bold';
		}
}
.icon-cart {
}

</style>

