<template>
    <section id="skill">
        <div class="skill__inner">
            <div class="skill__title">
                <h2>Front-end Developer<em>나의 도전</em></h2>
            </div>
            <div class="skill__desc">
                <div v-for="(skill, key) in skillText" :key="key">
                    <span>1. </span>
                    <h3>{{ skill.title }}</h3>
                    <p>
                        {{ skill.desc }}
                    </p>
                </div>
                <!-- <div>
                    <span>2. </span>
                    <h3>혁신을 통해 세상을 바꾸다</h3>
                    <p>
                        저는 혁신적인 아이디어를 통해 세상을 변화시키는 것을 목표로 합니다. 더 나은 사용자 경험을 제공하기 위해 끊임없이 연구하고, 배우고, 발전해 나가고 있습니다. 모든 픽셀 하나하나에
                        정성을 담아, 사용자가 웹을 통해 더 나은 세상을 경험할 수 있도록 노력합니다. 협업을 통해 더 나은 솔루션을 찾아내고, 다양한 관점을 수용하여 창의적인 해결책을 제시하는 것을
                        중요시합니다. 이러한 과정 속에서 성장하는 자신을 기대합니다.
                    </p>
                </div>
                <div>
                    <span>3. </span>
                    <h3>비전을 가지고 미래를 설계하다</h3>
                    <p>
                        제 비전은 웹 기술을 통해 사람들의 삶을 더 풍요롭게 만드는 것입니다. 사용자 중심의 디자인과 접근성을 고려한 코딩으로, 모든 이가 쉽게 접근하고 사용할 수 있는 웹을 만들고자
                        합니다. 끊임없는 학습과 자기계발을 통해 최신 기술을 습득하고, 이를 바탕으로 혁신적인 프로젝트를 구현해 나갈 것입니다. 협업과 소통을 통해 더 큰 목표를 이루며, 더 나은 미래를
                        설계하는데 기여하고 싶습니다. 이러한 비전을 실현하기 위해 오늘도 한 걸음 더 나아갑니다.
                    </p>
                </div> -->
            </div>
        </div>
    </section>
</template>

<script setup>
import { skillText } from '@/constants'
</script>

<style lang="scss" scoped>
#skill {
    min-height: 900px;
    background-color: #3f4d34;
}
.skill__inner {
    padding: 16px;
    display: flex;
    justify-content: space-between;

    @media (max-width: 800px) {
        flex-direction: column;
    }

    .skill__title {
        position: sticky;
        top: 100px;
        left: 0;
        width: 48%;
        height: 5vw;
        margin-top: 22px;

        @media (max-width: 800px) {
            width: 100%;
        }

        h2 {
            font-size: 4vw;
            font-weight: 900;
            line-height: 1;
            text-transform: uppercase;
            color: var(--white);
            font-family: var(--mainKor-font);
            border-bottom: 0.4vw solid var(--white);

            em {
                font-size: 1.25rem;
                line-height: 1.1;
                font-weight: 400;
                margin-left: 10px;
            }
        }
    }
    .skill__desc {
        width: 50%;

        @media (max-width: 800px) {
            width: 100%;
            margin-top: 22px;
        }

        span {
            font-size: 5vw;
            line-height: 1.3;
            font-weight: 900;
            font-family: var(--mainNum-font);
            color: var(--white);
        }

        h3 {
            font-size: 1.5rem;
            text-decoration: underline;
            text-underline-position: under;
            margin-bottom: 1vw;
            color: var(--white);
            line-height: 1.7;
        }

        p {
            margin-bottom: 30vh;
            font-size: 1.1rem;
            color: var(--white);
            line-height: 1.7;
        }
    }
}
</style>
