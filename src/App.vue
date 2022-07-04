<template>
    <div id="app">
        <div class="header">
            <div class="header__logo">
                <img src="./assets/header/riot games.png" alt="riot games logo">
                <div class="header__logo__bar"></div>
                <img src="./assets/header/valorant_logo.png" alt="valorant logo">
            </div>
            <div class="header__menu">
                <div>GAME</div>
                <div>CHAMPIONS</div>
                <div class="header__menu__defil">NEWS <img src="./assets/header/polygon.png" alt="polygon"></div>
                <div>PATCH NOTES</div>
                <div class="header__menu__defil">DISCOVER <img src="./assets/header/polygon.png" alt="polygon"></div>
                <div>ESPORTS</div>
                <div>UNIVERSE</div>
                <div>SHOP</div>
                <div>SUPPORT</div>
            </div>
            <div class="header__profile">
                <img src="./assets/header/profile_icon.png" alt="profile icon">
                <div>LeDjoo</div>
                <img src="./assets/header/polygon.png" alt="polygon">
            </div>
        </div>
        <div class="content">
            <div class="main__content">
                <div class="smgs">SMGS</div>
                <div class="main_block">
                    <div class="background"></div>
                    <div class="main_block_1">
                        <img src="./assets/content/Weapon_Spectre.png" alt="weapon spectre">
                        <div class="main_block_1_content">
                            <div class="text">
                                The Spectre has the better headshot damage: Two headshots to kill an armored enemy at 20 meters, and three shots at above 20 meters.
                            </div>
                            <div class="text">
                                Primary fire: Using Spectre primary fire is very good in close range and can stealth eliminate the enemy before they know where you shooting from.
                            </div>
                            <div class="text">
                                Alternative fire: When using alternative fire in Spectre, it turn on the scope that help reduce recoil, and improve accuracy a little, however the fire rate will drop to 12. Use Alternative fire when the enemy is far from you.
                            </div>
                            <div class="text">
                                Aim for Head: Using Spectre is better when you aim at head area because it can help eliminate the enemy quicker, aiming at body area is not very effective because of the fire rate is not that fast.
                            </div>
                            <div class="text">
                                Best time to use Spectre: The best time to use Spectre is in force buy rounds, or after you win pistol round.
                            </div>
                            <div class="imgs">
                                <img src="./assets/content/Luxe_Spectre_Level_1.png" alt="luxe spectre level 1">
                                <img src="./assets/content/Luxe_Spectre_Level_4.png" alt="luxe spectre level 4">
                            </div>
                        </div>
                    </div>
                    <div class="main_block_2">
                        <div class="block">
                            <div class="text">
                                <div class="text_block">
                                    <div class="text__title">
                                        Primary Fire
                                    </div>
                                    <div class="text__content">
                                        <span class="text__content_title">Fire Mode :</span> Full-Automatic
                                    </div>
                                    <div class="text__content">
                                        <span class="text__content_title">Rate of Fire :</span> 13.33 rounds/sec
                                    </div>
                                </div>

                                <div class="text_block">
                                    <div class="text__title">
                                        Alternative Fire
                                    </div>
                                    <div class="text__content">
                                        <span class="text__content_title">Fire Mode :</span> Zoom mode (1.15x) 
                                    </div>
                                    <div class="text__content">
                                        <span class="text__content_title">Rate of Fire :</span> 18 rounds/sec
                                    </div>
                                </div>

                                <div class="text_block">
                                    <div class="text__content">
                                        <span class="text__content_title">Magazine Capacity :</span> 30 
                                    </div>
                                    <div class="text__content">
                                        <span class="text__content_title">Wall Penetration :</span> Medium
                                    </div>
                                </div>
                            </div>
                            <div class="spectre">SPECTRE</div>
                        </div>
                        <img src="./assets/content/stream.png" alt="stream picture">
                    </div>
                </div>
            </div>
            <div class="items">
                <div class="item" v-for="(item, index) in items" :key="index">
                    <div class="text">
                        <div class="dmg">{{ item.dmg }} DMG</div>
                        <div class="portee">0 - 20 m</div>
                        <div class="desc">{{ item.desc }}</div>
                    </div>
                    <div class="img">
                        <img :src="item.img">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    name: 'App',

    data() {
        return {
            items: [
                {
                    dmg: 78,
                    desc: "Using Spectre is better when you aim at head area because it can help eliminate the enemy quicker.",
                    img: require("./assets/items/headshot.png")
                },
                {
                    dmg: 26,
                    desc: "Aiming at body area is not very effective because of the fire rate is not that fast.",
                    img: require("./assets/items/bodyshot.png")
                },
                {
                    dmg: 22,
                    desc: "Aiming at feet area is not very effective because of the fire rate is not that fast.",
                    img: require("./assets/items/feetshot.png")
                },
            ]
        }
    }
}
</script>

<style lang="scss">
#app {
    height: 100vh;
    width: 100vw;
}

.header {
    font-family: 'Montserrat Bold';
    font-size: 14px;
    background-color: rgb(31, 35, 38);
    color: white;
    height: 132px;
    width: 100%;

    display: flex;
    align-items: center;

    &__logo {
        display: flex;
        gap: 80px;
        padding: 0px 1% 0px 3%;
        width: 15%;

        &__bar {
            border: 1px solid white;
            height: 40px;
        }
    }

    &__menu {
        display: flex;
        align-items: center;
        gap: 75px;
        width: 70%;

        &__defil {
            display: flex;
            align-items: center;
            gap: 20px;
        }
    }

    &__profile {
        display: flex;
        align-items: center;
        width: 20%;
        justify-content: center;
        gap: 10px;
        padding-right: 50px;
    }
}

.main__content {
    display: flex;
    margin-left: 125px;
    background-image: url('./assets/content/elements.png');
    background-size: cover;
}

.content {
    background-image: url('./assets/content/background.png');
    background-size: cover;
    height: 1499px;
    background-color: #FF4656;

    & .smgs {
        font-size: 209px;
        font-weight: 500;
        line-height: 273px;
        font-family: 'Druk Wide';
        letter-spacing: 0.1em;
        -webkit-text-stroke: 2px white;
        color: transparent;
        writing-mode: vertical-rl;
        padding-top: 0.75em;
        padding-right: 0.25em;
        padding-bottom: 0.25em;
        padding-left: 0.5em;
    }
}

.main_block {
    width: 1978px;
    height: 1156px;
    display: flex;
    position: relative;

    & .background {
        background-image: url('./assets/content/background_main_block.png');
        background-size: cover;
        position: absolute;
        width: 91%;
        height: 86%;
        top: 5%;
        left: 5%;
    }

    &_1 {
        font-family: 'Montserrat Regular';
        padding-top: 5%;
        padding-left: 2%;
        font-size: 16px;
        font-weight: 400;
        line-height: 20px;
        width: 60%;
        z-index: 2;
        &_content {
            width: 100%;
            transform: translateY(-8%);
        }

        & .imgs {
            & img:first-child {
                margin-right: 56px;
            }
        }
        & div.text {
            margin-left: 7%;
            width: 90%;
            margin-bottom: 29px;
        }

        & div.text:nth-child(1) {
            width: 26% !important;
        }
    }

    &_2 {
        width: 40%;
        padding-left: 7%;
        z-index: 2;

        & .block {
            display: flex;
            & .text {
                padding-top: 16.5%;
                width: 50%;

                &_block {
                    margin-bottom: 30%;
                }

                &__title {
                    font-family: 'Druk Wide';
                    font-weight: 500;
                    font-size: 24px;
                    line-height: 31px;
                    color: #1F2326;
                    margin-bottom: 20%;
                }

                &__content {

                    font-weight: 500;
                    font-size: 14px;
                    line-height: 18px;
                    color: #1F2326;
                    font-family: 'Druk Wide';
                    &_title {
                        color: #C4C4C4;
                    }
                    margin-bottom: 9%;
                }
            }
        }

        & .spectre {
            width: 50%;
            text-align: center;
            display: flex;
            align-items: center;

            font-weight: 500;
            font-family: 'Druk Wide';
            letter-spacing: 0.1em;
            -webkit-text-stroke: 2px #F14251;
            color: transparent;
            writing-mode: vertical-rl;
            font-size: 90px;
            line-height: 117px;
            padding-top: 0.5em;
        }

        & img {
            width: 95%;
        }
    }
}

.items {
    display: flex;
    gap: 90px;
    justify-content: center;
    overflow: hidden;
    margin: 50px;

    & .item {
        background: #F8F8F8;
        border: 2px solid #000000;
        padding-left: 2%;
        padding-top: 1.5%;
        margin-bottom: 2%;
        display: flex;
        width: 654px;

        & .text {
            width: 50%;
        }

        & .dmg {
            font-family: 'Druk Wide';
            font-weight: 500;
            font-size: 40px;
            line-height: 52px;
            color: #C4C4C4;
            margin-bottom: 5%;
        }

        & .portee {
            font-family: 'Druk Wide';
            font-weight: 500;
            font-size: 24px;
            line-height: 31px;
            color: black;
            margin-bottom: 7%;
        }

        & .desc {
            font-family: 'Montserrat Regular';
            font-weight: 400;
            font-size: 16px;
            line-height: 20px;
            color: black;
            width: 95%;
        }

        & .img {
            width: 50%;
            display: flex;
            justify-content: center;
        }
    }
}
</style>
