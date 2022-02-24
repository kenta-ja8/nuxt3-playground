<template>
    <div class="scroll-area">
        <div class="parallax">
            <div class="parallax__layer parallax__layer__0">
                <img src="/parallax-scrolling/parallax0.png" />
            </div>
            <div class="parallax__layer parallax__layer__1">
                <img src="/parallax-scrolling/parallax1.png" />
            </div>
            <div class="parallax__layer parallax__layer__2">
                <img src="/parallax-scrolling/parallax2.png" />
            </div>
            <div class="parallax__layer parallax__layer__3">
                <img src="/parallax-scrolling/parallax3.png" />
            </div>
            <div class="parallax__layer parallax__layer__4">
                <img src="/parallax-scrolling/parallax4.png" />
            </div>
            <div class="parallax__layer parallax__layer__5">
                <img src="/parallax-scrolling/parallax5.png" />
            </div>
            <div class="parallax__layer parallax__layer__6">
                <img src="/parallax-scrolling/parallax6.png" />
            </div>
            <div class="parallax__layer parallax__layer__7">
                <img src="/parallax-scrolling/parallax7.png" />
            </div>
            <div class="parallax__layer parallax__layer__8">
                <img src="/parallax-scrolling/parallax8.png" />
            </div>

            <div class="parallax__cover">
                <div class="ref-area content">
                    <h3>参考・参照</h3>
                    <ol>
                        <li>
                            <a
                                target="_blank"
                                rel="noopener noreferrer"
                                href="https://www.firewatchgame.com/"
                            >https://www.firewatchgame.com/</a>
                        </li>
                        <li>
                            <a
                                target="_blank"
                                rel="noopener noreferrer"
                                href="https://www.firewatchgame.com/"
                            >https://www.firewatchgame.com/</a>
                        </li>
                        <li>
                            <a
                                target="_blank"
                                rel="noopener noreferrer"
                                href="https://codepen.io/samdbeckham/pen/OPXPNp"
                            >https://codepen.io/samdbeckham/pen/OPXPNp</a>
                        </li>
                        <li>
                            <a
                                target="_blank"
                                rel="noopener noreferrer"
                                href="https://ics.media/entry/210519/"
                            >https://ics.media/entry/210519/</a>
                        </li>
                    </ol>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
.ref-area {
    color: #ffaf1b !important;
    position: absolute;
    bottom: 5%;
    right: 5%;
    padding: 1rem;
}
.ref-area > h3,
a {
    color: #ffaf1b;
}
.scroll-area {
    height: 100%;
    width: 100%;
    background-color: #ffaf1b;
}
.parallax {
    perspective: 100px;
    perspective-origin: 50% 45%;
    height: 100%;
    overflow-x: hidden;
    overflow-y: auto;
    position: relative;
    top: 0;
}

.parallax__layer {
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: -10px;

    img {
        display: block;
        position: absolute;
        bottom: 0;
    }
}

.parallax__cover {
    background-color: #210002;
    display: block;
    position: absolute;
    top: 99%;
    left: 0;
    right: 0;
    height: 2000px;
    z-index: 2;
}

$parallax__layers: 8;

@for $i from 0 through $parallax__layers {
    $x: calc(($parallax__layers - $i) / 2);
    .parallax__layer__#{$i} {
        transform: translateZ((-100 * $x) + px) scale($x + 1);
    }
}
</style>