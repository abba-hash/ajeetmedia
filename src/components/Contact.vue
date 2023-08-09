<template>
    <section class="contact section ">
        <div class="contact-container grid container">
            <div class="contact-box">
                <h2 class="contact-title">
                    Reach out to us today <br> via any of the given <br> information
                </h2>

                <div class="contact-data">
                    <div class="contact-information">
                        <h3 class="contact-subtitle">Call us for instant support</h3>
                        <span class="contact-description">
                            <i class="fa-solid fa-phone contact-icon"></i>
                            +9576755575
                        </span>
                    </div>
                    <div class="contact-information">
                        <h3 class="contact-subtitle">Write us by mail</h3>
                        <span class="contact-description">
                            <i class="fa-solid fa-envelope contact-icon"></i>
                            info@ajeetmedia.com
                        </span>
                    </div>
                </div>
            </div>
            <form class="contact-form">
                <div class="contact-inputs">
                    <div class="contact-content">
                        <input type="email" placeholder=" " class="contact-input">
                        <label for="" class="contact-label">Email</label>
                    </div>
                    <div class="contact-content">
                        <input type="text" placeholder=" " class="contact-input">
                        <label for="" class="contact-label">Subject</label>
                    </div>
                     <div class="contact-content contact-area">
                        <textarea name="message" placeholder=" " class="contact-input"></textarea>
                        <label for="" class="contact-label">Message</label>
                    </div>
                </div>
                <button class="button button-flex">
                    Send Message
                    <box-icon type='solid' name='right-top-arrow-circle' class="button-icon"></box-icon>
                </button>
            </form>
        </div>
    </section>
</template>
<script>
export default {
    name: 'ContactVue'
}
</script>
<style lang="scss" scoped>
    .contact{
        margin-top: 4rem;
        background-color: antiquewhite;
    }
    .contact-container{
        row-gap: 3.5rem;
        @media screen and (min-width: 767px){
            grid-template-columns: repeat(2, 1fr);
        }
    }
    .contact-data{
        display: grid;
        row-gap: 2rem;
    }
    .contact-title{
        font-size: var(--h2-font-size);
        margin-bottom: var(--mb-2);
        line-height: 140%;
        @media screen and (min-width: 992px){
            font-size: var(--h1-font-size);
        }
    }
    .contact-subtitle{
        font-size: var(--normal-font-size);
        font-weight: var(--font-medium);
        color: var(--text-color);
        margin-bottom: var(--mb-0-5);
    }
    .contact-description{
        display: inline-flex;
        align-items: center;
        column-gap: .5rem;
        color: var(--title-color);
        font-weight: var(--font-medium);
    }
    .contact-icon{
        font-size: 1.25rem;
    }
    .contact-inputs{
        display: grid;
        row-gap: 2rem;
        margin-bottom: var(--mb-2-5);
    }
    .contact-content{
        position: relative;
        height: 3rem;
        border-bottom: 1px solid var(--text-color-light);
    }
    .contact-input{
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        padding: 1rem 1rem 1rem 0;
        background: none;
        color: var(--text-color);
        border: none;
        outline: none;
        z-index: 1;

        &:focus{
            +.contact-label{
                top: -.75rem;
                left: 0;
                font-size: var(--smaller-font-size);
                z-index: 10;
            }
        }
        &:not(:placeholder-shown){
            &:not(:focus){
                +.contact-label{
                    top: -.75rem;
                    font-size: var(--smaller-font-size);
                    z-index: 10;
                }
            }
        }
    }
    .contact-label{
        position: absolute;
        top: .75rem;
        width: 100%;
        font-size: var(--small-font-size);
        color: var(--text-color-light);
        transition: .3s;
    }
    .contact-area{
        height: 7rem;
        textarea{
            resize: none;
        }
    }
    .button-flex{
        display: inline-flex;
        align-items: center;
        column-gap: .5rem;
        margin-top: 2rem;
    }
    .button-icon{
        transition: .3s;
    }
</style>