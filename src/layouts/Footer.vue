<template>
    <div class="footer__wrapper">
        <div class="footer__container container">
            <div class="footer__body">
                <div class="footer__content">
                    <div class="footer__logo">
                        <img src="@/assets/img/logo-white.png" alt="">
                    </div>
                    <div class="footer__text">
                        Компания «Султан» — снабжаем розничные магазины товарами 
                        "под ключ" в Кокчетаве и Акмолинской области
                    </div>
                    <div class="footer__action">
                        <div class="footer__label">
                            Подпишись на скидки и акции
                        </div>
                        <form action="" class="footer__form form-footer">
                            <input type="text" placeholder="Введите ваш E-mail">
                            <button type="submit" class="form-footer__btn icon-down"></button>
                        </form>
                    </div>
                </div>
                <div class="footer__menu">
                    <ul class="footer__list">
                        <li class="footer__item">
                            <a class="footer__link footer-title">Меню сайта:</a>
                        </li>
                        <li class="footer__item">
                            <a href="" class="footer__link">О компании</a>
                        </li>
                        <li class="footer__item">
                            <a href="" class="footer__link">Доставка и оплата</a>
                        </li>
                        <li class="footer__item">
                            <a href="" class="footer__link">Возврат</a>
                        </li>
                        <li class="footer__item">
                            <a href="" class="footer__link">Контакты</a>
                        </li>
                    </ul>
                    <ul class="footer__list">
                        <li class="footer__item">
                            <a class="footer__link footer-title">Категории:</a>
                        </li>
                        <li class="footer__item">
                            <a href="" class="footer__link">Бытовая химия</a>
                        </li>
                        <li class="footer__item">
                            <a href="" class="footer__link">Косметика и гигиена</a>
                        </li>
                        <li class="footer__item">
                            <a href="" class="footer__link">Товары для дома</a>
                        </li>
                        <li class="footer__item">
                            <a href="" class="footer__link">Товары для детей и мам</a>
                        </li>
                        <li class="footer__item">
                            <a href="" class="footer__link">Посуда</a>
                        </li>
                    </ul>
                    <ul class="footer__list">
                        <li class="footer__item">
                            <a class="footer__link footer-title">Скачать прайс-лист:</a>
                        </li>
                        <li class="footer__item">
                            <a href="" class="footer__link link-footer-button">Прайс-лист
                                <span class="icon-download"></span>
                            </a>
                        </li>
                        <li class="footer__item">
                            <a href="" class="footer__link">Связь в мессенджерах:</a>
                        </li>
                        <li class="footer__item">
                            <div class="footer__social social-footer">
                                <a href="" class="social-footer__icon icon-whatsapp"></a>
                                <a href="" class="social-footer__icon tele">
                                    <span class="icon-telegram"></span>
                                </a>
                            </div>
                        </li>
                    </ul>
                    <ul class="footer__list">
                        <li class="footer__item">
                            <a class="footer__link footer-title">Контакты:</a>
                        </li>
                        <li class="footer__item contacts">
                            <div class="contacts__phone">+7 (777) 490-00-91</div>
                            <div class="contacts__data">время работы: 9:00-20:00</div>
                            <a href="" class="contacts__link">
                                Заказать звонок
                            </a>
                        </li>
                        <li class="footer__item">
                            <a href="" class="footer__link link-email">
                                <div class="footer__email">opt.sultan@mail.ru </div>
                                <div class="footer__email-text">На связи в любое время</div>
                            </a>
                        </li>
                        <li class="footer__item">
                            <div class="footer__social card-footer">
                                <a href="" class="card-footer">
                                    <img src="@/assets/img/visa.png" alt="">
                                </a>
                                <a href="" class="card-footer">
                                    <img src="@/assets/img/master.png" alt="">
                                </a>
                            </div>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>
<style lang="scss">
.footer{
    &__wrapper{
        background: #3F4E65;
        padding: 71px 0px 116px 0px;
    }
}
.footer {

		// .footer__container

		&__container {
		}

		// .footer__body

		&__body {
            display: flex;
            justify-content: space-between;
		}

		// .footer__content

		&__content {
            flex: 0 0 320px;
            margin-right: 60px;
		}

		// .footer__logo

		&__logo {
            margin-bottom: 15px;
            & img{
                width: 156px;
            }
		}

		// .footer__text

		&__text {
            color: #fff;
            font-size: 16px;
            line-height: 24/16*100%;
            margin-bottom: 45px;
		}

		// .footer__action

		&__action {
		}

		// .footer__label

		&__label {
            color: #fff;
            font-size: 12px;
            margin-bottom: 14px;
		}

		// .footer__form

		&__form {
            & input{
                width: 84%;
                border: unset;
                &:focus{
                    outline: none;
                }
            }
            background: #fff;
            padding: 10px 10px 10px 20px;
            border-radius: 79px;
            max-width: 282px;
		}

		// .footer__menu

		&__menu {
            display: flex;
            justify-content: space-between;
            flex: 1 1 auto;
		}

		// .footer__list

		&__list {
		}

		// .footer__item

		&__item {
            &:not(:last-child){
                margin-bottom: 20px;
            }
		}

		// .footer__link

		&__link {
            color: #fff;
            line-height: 21/14*100%;
		}

		// .footer__social

		&__social {
            display: flex;
		}

		// .footer__email

		&__email {
            font-size: 12px;
            font-family: 'i-bold';
            line-height: 100%;
		}

		// .footer__email-text

		&__email-text {
            font-size: 12px;
            line-height: 100%;
		}
}
.link-email{
    line-height: unset;
}

.form-footer {

		// .form-footer__btn

		&__btn {
            width: 39px;
            height: 39px;
            border-radius: 50%;
            border: unset;
            background: #FFC85E;
            align-items: center;
            color: #fff;
		}
}
.icon-down {
    transform: rotate(180deg);
}
.footer-title {
    color: #fff;
    font-family: 'i-bold';
    font-size: 20px;
    margin-bottom: 25px;
    display: inline-block;
}
.link-footer-button {
    background: #FFC85E;
    padding: 21px;
    width: 214px;
    border-radius: 79px;
    display: inline-block;
    text-align: center;
    font-size: 14px;
}
.icon-download {
    margin-left: 15px;
}
.social-footer {
    &:not(:last-child){
        margin-right: 10px;
    }
    &__icon{
        width: 39px;
        height: 39px;
        border-radius: 50%;
        background: #00E676;
        padding: 8px;
        display: inline-block;
        &.tele{
            position: relative;
            background:#40B3E0;
            & span{
                top: 8px;
                left: 4px;
                position: absolute;
            }
        }
    }
    
}
.icon-whatsapp {
    display: block;
    color: #fff;
    font-size: 23px;
    margin-right: 10px;
    
}
.icon-telegram {
    display: block;
    color: #fff;
    font-size: 23px;
    background:#40B3E0;
}
.contacts {

		// .contacts__phone

		&__phone {
            color: #fff;
            font-size: 14px;
            font-family: 'i-medium';
            font-weight: 600;
		}

		// .contacts__data

		&__data {
            color: #fff;
            font-size: 12px;
            margin: 5px 0px;
		}

		// .contacts__link

		&__link {
            color: #fff;
            font-size: 10px;
            margin-bottom: 25px;
            @media (any-hover:hover) {
                &:hover{
                    text-decoration: underline;
                }
                
            }
		}
}
.card-footer {
    margin-right: 5px;
}

</style>