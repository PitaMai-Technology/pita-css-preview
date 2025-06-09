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
                <h2>検索</h2>
                <form class="w-max768 search-box">
                    <input type="search" placeholder="キーワードを入力してください..." />
                    <button type="submit">検索</button>
                </form>
                <button data-theme-toggle class="theme-toggle-btn mY20">🔄</button>
                <select data-theme-select class="mT20">
                    <option value="auto">💻 システム設定</option>
                    <option value="light">☀️ ライト</option>
                    <option value="dark">🌙 ダーク</option>
                </select>
            </div>

            <!-- メニューリスト -->
            <ul>
                <li>
                    <NuxtLink href="/">ホーム</NuxtLink>
                </li>
                <li>
                    <NuxtLink href="/low-class">低水準Class</NuxtLink>
                </li>
                <li>
                    <NuxtLink href="/height-class">ハイレベルClass</NuxtLink>
                </li>
                <li>
                    <NuxtLink href="#">ローディング(SSR)</NuxtLink>
                    <!-- ネストされたメニュー -->
                    <ul>
                        <li>
                            <NuxtLink href="/1s">1秒</NuxtLink>
                        </li>
                        <li>
                            <NuxtLink href="/3s">3秒</NuxtLink>
                        </li>
                    </ul>
                </li>
                <li>
                    <NuxtLink href="/">ホーム</NuxtLink>
                </li>
                <li>
                    <NuxtLink href="#">ID(#)</NuxtLink>
                </li>
            </ul>
        </aside>
    </div>
</template>

<style>
</style>