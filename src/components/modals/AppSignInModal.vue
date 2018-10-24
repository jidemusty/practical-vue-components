<template>
    <AppModal name="signin">
        <template slot="body" slot-scope="{ params }">
            Sign in {{ params.name }}
        </template>
    </AppModal>
</template>

<script>
import AppModal from "@/components/AppModal";

export default {
    components: {
        AppModal
    }
};
</script>

<style>
</style>
