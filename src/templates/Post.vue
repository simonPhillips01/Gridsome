<template>
    <Layout>
        <div v-html="$page.post.content"/>
        <vue-disqus shortname="gridsome-3" :identifier="$page.post.id"></vue-disqus>
    </Layout>
</template>

<page-query>
    query($path: String!) {
        post (path: $path) {
            content
        }
    }
</page-query>