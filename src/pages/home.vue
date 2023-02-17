<template>
    <f7-page name="home">
        <!-- Top Navbar -->
        <f7-navbar :sliding="false">
            <f7-nav-left>
                <f7-link icon-ios="f7:menu" icon-aurora="f7:menu" icon-md="material:menu" panel-open="left"></f7-link>
            </f7-nav-left>
            <f7-nav-title>My App</f7-nav-title>
        </f7-navbar>
        <!-- Toolbar-->
        <f7-toolbar bottom>
            <f7-link>Left Link</f7-link>
            <f7-link>Right Link</f7-link>
        </f7-toolbar>
        <!-- Page content-->
        <f7-block strong inset>
            <p>This is an example of split</p>

            <p>Each view may have different layout, different navbar type (dynamic, fixed or static) or without
                navbar.</p>

            <p>The fun thing is that you can easily control one view from another without any line of JavaScript just
                using "data-view" attribute on links.</p>
        </f7-block>
        <f7-block-title>Navigation</f7-block-title>
        <f7-list inset>
            <f7-list-item link="/about/" title="About"></f7-list-item>
            <f7-list-item link="/form/" title="Form"></f7-list-item>
        </f7-list>

        <f7-block-title>Modals</f7-block-title>
        <f7-block strong inset>
            <f7-row>
                <f7-col width="50">
                    <f7-button fill raised popup-open="#my-popup">Popup</f7-button>
                </f7-col>
                <f7-col width="50">
                    <f7-button fill raised login-screen-open="#my-login-screen">Login Screen</f7-button>
                </f7-col>
            </f7-row>
        </f7-block>

        <f7-block-title>Panels</f7-block-title>
        <f7-block strong inset>
            <f7-row>
                <f7-col width="50">
                    <f7-button fill raised panel-open="left">Left Panel</f7-button>
                </f7-col>
                <f7-col width="50">
                    <f7-button fill raised panel-open="right">Right Panel</f7-button>
                </f7-col>
            </f7-row>
        </f7-block>

        <f7-list inset>
            <f7-list-item
                title="Dynamic (Component) Route"
                link="/dynamic-route/blog/45/post/125/?foo=bar#about"
            ></f7-list-item>
            <f7-list-item
                title="Default Route (404)"
                link="/load-something-that-doesnt-exist/"
            ></f7-list-item>
            <f7-list-item
                title="Request Data & Load"
                link="/request-and-load/user/123456/"
            ></f7-list-item>
        </f7-list>
    </f7-page>
</template>
<script>
import {ref, onMounted} from 'vue';
import {getDevice} from '../js/framework7-custom.js';

export default {
    setup() {
        const device = getDevice();

        onMounted(() => {

        });

        return {
        }
    }
}
</script>