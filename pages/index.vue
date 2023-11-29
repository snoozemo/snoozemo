<template>
    <main class="md:w-[960px]  w-5/6 m-auto mt-32 font-thin space-y-10">
        <div class="space-y-10">
            <p class="text-3xl font-thin p5-outlinetext-white">
                我是再躺一会儿吧，一名前端开发者，也会一点 c# 和 flutter。
            </p>
            <p class="underline text-right">
                <a class="leading-normal" href="mailto:master@snoozemo.com">{{ "发送电子邮件给 <master@snoozemo.com>"
                }}</a>
            </p>
        </div>
        <svg width="0" height="0">
            <filter id="outline">
                <feMorphology in="SourceAlpha" result="DILATED" operator="dilate" radius="2" />
                <feFlood floodColor="#fff" floodOpacity="1" result="flood" />
                <feComposite in="flood" in2="DILATED" operator="in" result="OUTLINE" />
                <feMerge>
                    <feMergeNode in="OUTLINE" />
                    <feMergeNode in="SourceGraphic" />
                </feMerge>
            </filter>
        </svg>
        <NuxtPage />
    </main>
</template>
<script setup lang='ts'>

</script>
<style scoped>
.p5-outline {
    filter: url(#outline);
    -webkit-filter: url(#outline);
}
</style>