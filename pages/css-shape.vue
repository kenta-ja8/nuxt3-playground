<template>
    <section>
        <div class="display-box box" data-label="フロー">
            <div class="flow">
                <span class="arrorw">5分</span>
                <span class="spot">A</span>
                <span class="arrorw">115分</span>
                <span class="spot">B</span>
                <span class="arrorw">10分</span>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
.display-box {
    position: relative;
    margin-top: 1rem;
    padding: 1rem;
    margin: 2rem;
    &::before {
        content: attr(data-label) "";
        font-size: 1.5rem;
        position: absolute;
        top: 0;
        left: 0.4rem;
        transform: translate(0, -50%);
        text-align: center;
    }

    > .flow {
        display: flex;
        align-items: center;
        > .arrorw {
            background-color: #e1e1e1;
            width: 30px;
            font-size: 12px;
            text-align: center;
            display: inline-block;
            position: relative;
            margin-right: 15px;
            margin-left: 5px;

            align-items: center;
            display: inline-flex;
            font-weight: bold;
            justify-content: center;
            &::after {
                content: "";
                width: 0;
                height: 0;
                position: absolute;
                left: 30px;
                border-top: solid 15px transparent;
                border-bottom: solid 15px transparent;
                border-left: solid 15px #e1e1e1;
            }
        }
        > .spot {
            background-color: #d4e7ff;
            border-radius: 50%;
            font-size: 20px;
            height: 30px;
            width: 30px;
            text-align: center;

            align-items: center;
            display: inline-flex;
            font-weight: bold;
            justify-content: center;
        }
    }
}
</style>