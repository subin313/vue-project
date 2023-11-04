<script setup>
import { footerText } from '../constants';
</script>
<template>
    <footer id="footer" role="contentinfo">
        <div class="footer__inner">
            <div class="footer__text">
                <span>subinggood</span>
                <span>@web</span>
            </div>
            <div class="footer__info">
                <div class="left">
                    <div class="title">
                        <a href="#">sign up</a>
                    </div>
                    <p class="desc">회원가입을 하시면 댓글과 게시판을 이용할 수 있습니다.</p>
                </div>
                <div class="right">
                    <h3>social</h3>
                    <ul>
                        <li v-for="(footer,key) in footerText" :key="key">
                            <a href="footer.link">{{footer.title}}</a>
                            <em>{{footer.desc}}</em>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="footer__right">
                @2023 subinggood<br>
                이 사이트는 비트를 이용하여 제작하였습니다.
            </div>
        </div>
    </footer>
</template>
<style lang="scss">
#footer{
    font-family: var(--mainKor-font);
}
.footer__inner{
    padding: 16px;
    .footer__text{
        width: 100%;
        display: flex;
        justify-content: space-between;
        border-top: 1px solid var(--black);
        border-bottom: 1px solid var(--black);
        font-size: 0.8rem;
        font-weight: 400;
        text-transform: uppercase;
    }
    .footer__info{
        display: flex;
        justify-content: space-between;
        margin: 100px 0;
        @media (max-width: 800px) {
            flex-direction: column;
        }
    }
    .footer__info .left{
        width: 40%;
        @media (max-width: 800px) {
            width: 100%;
        }
    }
    .footer__info .left .title{
        padding: 20px 0;
        border-top: 2px solid var(--black);
        border-bottom: 1px solid var(--black);
        font-weight: 700;
        text-transform: uppercase;
        background:url(../assets/img/arrow.svg) no-repeat right 20px;
        transition: all 0.3s;
        &:hover{
            background-color: var(--black400);
            padding-left: 10px;
            border-color: transparent;
        }
    }
    .footer__info .left p{
        font-size: 12px;
        padding-top: 20px;
        @media (max-width:800px) {
            margin-bottom: 40px;
        }
    }

}
.right{
    width: 50%;
    @media (max-width:800px) {
        width: 100%;
    }
    h3{
        padding: 10px 0 40px 0;
        font-size: 12px;
        border-top: 2px solid var(--black);
    }
        ul{
            border-top: 1px solid var(--black);
            li{
                border-bottom: 1px solid var(--black);
                a{
                    padding: 14px 0;
                    font-size: 14px;
                    display: inline-block;
                    text-transform: uppercase;
                }
                em{
                    opacity: 0;
                    padding-left: 10px;
                    transition: all 0.3s;
                    
                }
                &:hover{
                    em{
                        opacity: 1;
                    }
                }
            }
        }

}
.footer__right{
    width: 100%;
    height: 10vh;
    display: flex;
    justify-content: center;
    align-items: center;
    font-weight: 400;
    font-family: var(--mainKor-font);
    font-size: 12px;
    text-align: center;
    text-transform: uppercase;
}
</style>