<template>
    <div class="container article-tab">
        
        <nav>
            <div class="nav nav-tabs" id="nav-tab" role="tablist">
                <button class="nav-link active" id="nav-published-tab" data-bs-toggle="tab" data-bs-target="#nav-published"
                    type="button" role="tab" aria-controls="nav-published" aria-selected="true">Published</button>
                <button class="nav-link" id="nav-draft-tab" data-bs-toggle="tab" data-bs-target="#nav-draft"
                    type="button" role="tab" aria-controls="nav-draft" aria-selected="false">Draf</button>
                <button class="nav-link" id="nav-archived-tab" data-bs-toggle="tab" data-bs-target="#nav-archived"
                    type="button" role="tab" aria-controls="nav-archived" aria-selected="false">Archived</button>
                <button class="nav-link" id="nav-saved-tab" data-bs-toggle="tab" data-bs-target="#nav-saved"
                    type="button" role="tab" aria-controls="nav-saved" aria-selected="false">Saved</button>
            </div>
        </nav>
        <div class="tab-content" id="nav-tabContent">
            <div class="tab-pane fade show active" id="nav-published" role="tabpanel" aria-labelledby="nav-published-tab"
                tabindex="0">
                <ArticleList></ArticleList>
            </div>
            <div class="tab-pane fade" id="nav-draft" role="tabpanel" aria-labelledby="nav-draft-tab"
                tabindex="0">
                <ArticleList></ArticleList>
            </div>
            <div class="tab-pane fade" id="nav-archived" role="tabpanel" aria-labelledby="nav-archived-tab"
                tabindex="0">
                <ArticleList></ArticleList>
            </div>
            <div class="tab-pane fade" id="nav-saved" role="tabpanel" aria-labelledby="nav-saved-tab"
                tabindex="0">
                <ArticleList></ArticleList>
            </div>
        </div>
    </div>
</template>

<script>
import ArticleList from './ArticleList.vue'

export default {
    name: 'App',
    components: {
        ArticleList
    }
}
</script>

<style scoped>
.article-tab {
    position: relative;
    left: 2%;
    top: 3%;
    border: none;
}

#nav-tab {
    width: 90%;
    border-bottom: solid 1.2px black;
}

.nav-tabs {
    --bs-nav-tabs-border-width: 1px;
    --bs-nav-tabs-border-color: #dee2e6;
    --bs-nav-tabs-border-radius: 0;
    --bs-nav-tabs-link-hover-border-color: black;
    --bs-nav-tabs-link-active-color: #495057;
    --bs-nav-tabs-link-active-bg: rgba(245, 245, 245, 1);
    --bs-nav-tabs-link-active-border-color: black;
    border-bottom: 2px solid var(--bs-nav-tabs-border-color);
}

.nav-tabs .nav-link {
    margin-bottom: calc(-1 * var(--bs-nav-tabs-border-width));
    background: none;
    border: none;
}

.nav-tabs .nav-link.active,
.nav-tabs .nav-item.show .nav-link {
    color: var(--bs-nav-tabs-link-active-color);
    background-color: var(--bs-nav-tabs-link-active-bg);
    border-color: var(--bs-nav-tabs-link-active-border-color);
}

.nav-link {
    color: #000;
    border-top: 0;
    border-bottom: solid 1px black;
}

.nav-link:active {
    border-bottom: solid 2px black;
    color: rgba(0, 0, 0, 1);
}

.nav-link:focus {
    border-bottom: solid 1.5px black;
    color: #000;
}

.nav-link:hover {
    background-color: inherit;
    border-bottom: solid 1.5px black;
    color: #000;
}

.tab-pane {
    height: 100vh;
    width: 95%;
}
</style>