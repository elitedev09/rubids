<template>
<div class="sec-padding-a section-fulldark">
    <div class="container foot-region">
        <div class="row">
            <div class="col-md-12 col-xs-12 footer-tos col-centered text-left">
                <a href='#'><span>ToS</span></a>
                <a href='#'><span>Fairness</span></a>
                <a href='#'><span>VIP</span></a>
                <a href='#'><span>Club</span></a>
                <a href='#'><span>AML</span></a>
                <a href='#'><span>Responsible Gambling</span></a>
                <div class="pull-right language">
                    <img src="images/england.png"/><span>English</span>
                </div>
            </div>
            <div class="col-md-12 col-centered text-left">
                <p>roobet.com is a brand name of TekHou5 Limited, Reg No 171902, having its registered address at 9 Barrack Road, Belize City, Belize,</p>
                <p>licensed to conduct online gaming operations by the Government of Curacao under license 365/JAZ, sub-license GLH-OCCHKTW0710102018.</p>
                <p>Hou5Game Limited, Reg No. HE 391142, having its registered address at 1, Avlonos, Maria House, Nicosia, 1075 Cyprus, is a wholly owned</p>
                <p>subsidiary of TekHou5 Limited, which provides management, payment and support services related to the operation of the website. 18+ to play</p>
            </div>
            <div class="footer-logo col-md-12 col-centered text-left">
                <div class="col-md-2">
                    <img src="images/logo1.png"/>
                </div>
                <div class="col-md-10">
                    <span>complaints@gaming-curacao.com</span>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
  name: 'Footer',
  props: {
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.footer-tos a{
    color: white;
    padding: 0;
    font-size: 1rem;
    min-width: 0;
    font-family: "Roboto", "Helvetica", "Arial", sans-serif;
    font-weight: 500;
    line-height: 1.5;
    margin-right: 16px;
    border-radius: 0;
    letter-spacing: 0.00938em;
    display: inline-flex;
}
.footer-tos a span{
    font-size: 20px;
}
.language{
font-size: 2rem;
margin-left:5px;
}
@media only screen and (max-width: 1000px) {
    .language{
        width : 100%;
        text-align: right;
        margin-top: 10px;
		margin-bottom: 10px;
    }
    .tab_city button{
        padding: 6px 7px;
        margin: 2px 9px;
        font-size:20px;
    }
    .footer-logo{
        text-align: center;
    }
}
</style>
