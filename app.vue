<script setup>

let progressLoader = null

onMounted(async () => {
  // クライアントサイドでのみpita-css/jsをインポートして初期化
  const pitaModule = await import('pita-css/js')
  const AsideNav = pitaModule.default
  
    AsideNav?.init()
})

onUnmounted(() => {
  progressLoader?.destroy()
})

// const isLoading = ref<boolean>(false);
// const progressValue = ref<number>(0);
// let loadingStart: number = 0;
// let progressInterval: NodeJS.Timeout | null = null;
// let finalInterval: NodeJS.Timeout | null = null;

// const router = useRouter();

// // プログレスバーをクリアする関数
// const clearIntervals = (): void => {
//     if (progressInterval) {
//         clearInterval(progressInterval);
//         progressInterval = null;
//     }
//     if (finalInterval) {
//         clearInterval(finalInterval);
//         finalInterval = null;
//     }
// };

// // ローディング完了処理
// const finishLoading = (): void => {
//     const elapsed: number = Date.now() - loadingStart;
//     const minDuration: number = 800; // 最小表示時間を短縮

//     clearIntervals();

//     // プログレスバーを100%まで素早く完了
//     progressValue.value = 100;
    
//     // 最小表示時間を考慮してローディングを終了
//     const remainingTime: number = Math.max(0, minDuration - elapsed);
    
//     setTimeout(() => {
//         isLoading.value = false;
//         // progressValue.value = 0; // この行を削除して100で維持
//     }, remainingTime);
// };

// // ページ遷移開始時
// router.beforeEach((to, from, next) => {
//     // 現在のページと同じパスの場合はプログレスバーを表示しない
//     if (to.path === from.path) {
//         next();
//         return;
//     }
    
//     // 内部リンク（ハッシュのみの変更）の場合はプログレスバーを表示しない
//     if (to.path === from.path && to.hash !== from.hash) {
//         next();
//         return;
//     }
    
//     // 既存のローディングをクリア
//     clearIntervals();
    
//     isLoading.value = true;
//     progressValue.value = 5; // 新しい遷移開始時のみリセット
//     loadingStart = Date.now();

//     // プログレスバーのアニメーション開始
//     progressInterval = setInterval(() => {
//         const elapsed: number = Date.now() - loadingStart;
//         const estimatedDuration: number = 2000;
        
//         // より自然な進行曲線
//         const progress: number = Math.min(5 + (elapsed / estimatedDuration) * 85, 90);
//         progressValue.value = progress;
        
//         // 90%に達したら一旦停止
//         if (progress >= 90) {
//             clearInterval(progressInterval!);
//             progressInterval = null;
//         }
//     }, 16); // 60FPSに近い滑らかさ

//     next();
// });

// // ページの読み込み完了を監視
// const nuxtApp = useNuxtApp();
// nuxtApp.hook('page:finish', () => {
//     // 少し遅延を入れてDOM更新を確実に待つ
//     setTimeout(() => {
//         finishLoading();
//     }, 100);
// });

// // コンポーネントのアンマウント時にクリーンアップ
// onUnmounted(() => {
//     clearIntervals();
// });

// useHead({
//     link: [
//         { rel: "icon", href: "/favicon.png" },
//     ],
//     htmlAttrs: {
//         lang: 'ja'
//     },
// })


</script>

<template>
    <div>
        <NuxtLayout>
            <NuxtRouteAnnouncer />
            <NuxtPage />
        </NuxtLayout>
    </div>
</template>

<style scoped>
#progress {
    position: fixed;
    top: 0;
    left: 0;
    height: 3px;
    z-index: 1000;
    width: 100%;
    border-radius: 0 !important;
}

.fade-enter-active {
    transition: opacity 0.2s ease-in;
}

.fade-leave-active {
    transition: opacity 0.5s ease-out;
}

.fade-enter-from,
.fade-leave-to {
    opacity: 0;
}
</style>