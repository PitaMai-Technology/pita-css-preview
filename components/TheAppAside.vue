<script setup>
</script>

<template>
      <div>
            <button class="nav-toggle">☰</button>

            <!-- オーバーレイ（モバイル用） -->
            <div class="nav-overlay"></div>

            <!-- アサイドナビゲーション -->
            <aside>
                <!-- ナビヘッダー -->
                <div class="aside-header">
                    <h2>メニュー</h2>
                </div>

                <!-- メニューリスト -->
                <ul>
                    <li>
                        <NuxtLink href="/" class="active">ホーム</NuxtLink>
                    </li>
                    <li>
                        <NuxtLink href="/nav">商品情報</NuxtLink>
                    </li>
                    <li>
                        <NuxtLink href="#">サービス</NuxtLink>
                        <!-- ネストされたメニュー -->
                        <ul>
                            <li>
                                <NuxtLink href="/test">Webデザイン</NuxtLink>
                            </li>
                            <li>
                                <NuxtLink href="#">システム開発</NuxtLink>
                            </li>
                            <li>
                                <NuxtLink href="#">コンサルティング</NuxtLink>
                            </li>
                        </ul>
                    </li>
                    <li>
                        <NuxtLink href="#">会社概要</NuxtLink>
                    </li>
                    <li>
                        <NuxtLink href="#">お問い合わせ</NuxtLink>
                    </li>
                </ul>
            </aside>
        </div>
</template>