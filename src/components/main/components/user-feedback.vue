<template>
  <section>
    <div class="mx-auto">
      <div class="my-5">
        <h2>用户反馈</h2>
        <div class="mt-5">
          <p>如果您正在使用 Earthworm ，请随时在 Twitter 上向我们提供您的反馈!</p>
        </div>
        <div class="mt-5"></div>
      </div>
      <div class="mt-8">
        <div class="mb-8" v-for="card in cardInfos" :key="card.account">
          <blockquote>
            <div class="flex">
              <div class="gap-4">
                <!-- 头像显示 -->
                <img :src="card.avatar" class="avatar" />
                <div class="flex-grow">
                  <!-- 用户名 -->
                  <p class="text-lg">{{ card.username }}</p>
                  <!-- 账号名 -->
                  <p class="text-xs">{{ card.account }}</p>
                </div>
                <img width="30" class="self-start" src="@/assets/svgs/twitter.svg" alt="" />
              </div>
              <p class="mt-4">
                {{ card.content }}
              </p>
              <div class="my-2">
                <div class="text-gray-500">{{ card.date }}</div>
              </div>
              <div class="my-4"></div>
              <div class="justify-between">
                <div class="items-center">
                  <svg class="w-5 h-5 mr-2 fill-current text-pink-300 dark:text-blue-300" viewBox="0 0 24 24">
                    <path
                      d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"></path>
                  </svg>
                  <span>{{ card.likes }} likes</span>
                </div>
                <a>See cuixiaorui's</a>
              </div>
            </div>
          </blockquote>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup>
interface CardInfo {
  avatar: string
  username: string
  account: string
  content: string
  date: string
  likes: number
}
const cardInfos: CardInfo[] = [
  {
    avatar: '/src/assets/commentsImgs/cuixiaorui.jpg',
    username: 'cuixiaorui',
    account: '@cuixiaorui',
    content:
      'Earthworm 不仅仅是一个工具;这是一次进入语言学习核心的旅程，让每个句子和连词都成为一次冒险。凭借其令人上瘾的游戏玩法，它不仅是一种练习，而且是一种日常习惯，邀请您更深入地了解英语的丰富性！',
    date: '6:06 PM · Feb 20, 2024',
    likes: 1342,
  },
  {
    avatar: '/src/assets/commentsImgs/fengstats.png',
    username: 'fengstats',
    account: '@fengstats',
    content:
      '我简直被这款应用迷住了！这种渐进式的学习方式，让每个阶段都充满挑战，同时也让我有了一种强烈的成就感。我已经不能停下学习的脚步，我渴望一点点的进步，希望能更上一层楼！',
    date: '2:17 PM · Feb 20, 2024',
    likes: 197,
  },
  {
    avatar: '/src/assets/commentsImgs/zclsx.jpg',
    username: 'zclsx',
    account: '@jiushi21',
    content: '这个应用克服了英语学习的枯燥，我现在刷课程刷得停不下来。',
    date: '6:31 PM · Jan 23, 2024',
    likes: 79,
  },
  {
    avatar: '/src/assets/commentsImgs/Nauxscript.jpg',
    username: 'Nauxscript',
    account: '@Nauxscript',
    content:
      '现在我每天都要浏览这个应用程序，我觉得我的英语突飞猛进，有趣又充满成就感。我希望能够加入和我一样学习后进行打卡分享，会上瘾的！',
    date: '11:38 AM · Feb 3, 2024',
    likes: 520,
  },
  {
    avatar: '/src/assets/commentsImgs/yaolifeng0629.jpg',
    username: 'Ims',
    account: '@Immersecode',
    content: '如此有趣又充实的英语学习应用，真是让人不知所措。我现在每天都在练习，这已经成为一种习惯。棒！',
    date: '4:51 PM · Feb 2, 2024',
    likes: 98,
  },
  {
    avatar: '/src/assets/commentsImgs/vampirewy.jpg',
    username: 'vampirewy',
    account: '@vampirewy',
    content:
      '通过句子拆分进行学习，我感觉我刷课之后，对句子的理解更加深刻。这种感觉是潜移默化的，当我第二天打开，每次都会变得更加流畅！',
    date: '9:22 AM · Jan 9, 2024',
    likes: 86,
  },
  {
    avatar: '/src/assets/commentsImgs/hildxd.jpg',
    username: 'hildxd',
    account: '@hildxd',
    content:
      '再也没有像现在这样，我对学习如此充满热情。这个应用真是把学习变得如此有趣，每一次学习都像是一种挑战，让我无法抗拒。这种感觉太棒了，我能够一直刷课程而不觉得无聊',
    date: '11:56 PM · Mar 8, 2024',
    likes: 486,
  },
  {
    avatar: '/src/assets/commentsImgs/zuowendong.jpg',
    username: 'zuowendong',
    account: '@zuowendong',
    content:
      '我真的无法抵抗这款连词造句的英语学习应用的魔力，每天闲下来的时候，我都会习惯性地打开这款应用，忍不住去挑战一下自己，这对我来说是一种全新的娱乐方式！',
    date: '9:59 AM · Feb 22, 2024',
    likes: 232,
  },
  {
    avatar: '/src/assets/commentsImgs/Hazel-Lin.jpg',
    username: 'Hazel-Lin',
    account: '@HazelLin',
    content: '真没想到学习英语可以这么有趣，这个连词造句的方式简直让我停不下来。',
    date: '4:10 AM · Dec 22, 2023',
    likes: 78,
  },
]
</script>

<style scoped>
section {
  display: flex;
  flex-direction: column;
  padding-top: 96px;
  .mx-auto {
    max-width: 1280px;
    margin: 0 auto;

    .my-5 {
      text-align: center;
      margin: 20px 0;

      .mt-5 {
        margin-top: 20px;

        p {
          font-size: 20px;
          padding-top: 8px;
          color: var(--color-text-info);
        }
      }
    }
    .mt-8 {
      gap: 32px;
      column-count: 3;
      margin-top: 32px;

      div.mb-8 {
        margin-bottom: 32px;
        break-inside: avoid;

        blockquote {
          box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -4px rgba(0, 0, 0, 0.1);
          background-color: var(--background-color);
          border-radius: 8px;
          cursor: pointer;
          overflow: hidden;
          transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);

          .flex {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            height: 100%;
            padding: 24px;

            .gap-4 {
              display: flex;
              gap: 16px;
              align-items: center;

              .avatar {
                padding: 4px;
                object-fit: cover;
                border: 2px var(--color-icon-info) solid;
                border-radius: 9999px;
                width: 56px;
                height: 56px;
                vertical-align: middle;
              }
              .flex-grow {
                flex-grow: 1;
                text-align: left;
                p.text-lg {
                  font-weight: 700;
                  font-size: 18px;
                  line-height: 28px;
                  margin-top: 2px;
                  color: var(--color-text-header);
                }
                p.text-xs {
                  font-size: 12px;
                  line-height: 16px;
                  color: var(--color-text);
                }
              }
              .self-start {
                align-self: flex-start;
                vertical-align: middle;
              }
            }
            .mt-4 {
              text-align: left;
              color: var(--color-text-p-userfeed);
              font-size: 16px;
              line-height: 24px;
              margin-top: 16px;
            }
            .my-2 {
              display: flex;
              justify-content: space-between;
              align-items: center;
              margin: 8px 0;
            }
            .my-4 {
              margin: 16px 0;
            }
            div.justify-between {
              font-size: 12px;
              line-height: 16px;
              display: flex;
              justify-content: space-between;
              align-items: center;
              margin-top: 16px;

              .items-center {
                display: flex;
                align-items: center;

                svg {
                  width: 20px;
                  height: 20px;
                  margin-right: 20px;
                  vertical-align: middle;
                  fill: currentColor;
                  color: var(--color-svg-userfeed);
                }
                span {
                  color: var(--color-like-userfeed);
                }
              }
              a {
                pointer-events: none;
                color: var(--color-a-userfeed);
              }
            }
          }
        }
        blockquote:hover {
          box-shadow: 0 0 #0000, 0 0 #0000, 0 25px 50px -12px var(--color-card-shadow-userfeed);
        }
      }
    }
  }
}
</style>
