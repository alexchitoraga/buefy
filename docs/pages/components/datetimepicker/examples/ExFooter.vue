<template>
    <b-field label="Select datetime">
        <b-datetimepicker v-model="datetime"
            placeholder="Click to select...">

            <template slot="left">
                <b-button
                    label="Now"
                    type="is-primary"
                    icon-left="clock"
                    @click="datetime = new Date()" />
            </template>

            <template slot="right">
                <b-button
                    label="Clear"
                    type="is-danger"
                    icon-left="close"
                    outlined
                    @click="datetime = null" />
            </template>
        </b-datetimepicker>
    </b-field>
</template>

<script>
    export default {
        data() {
            return {
                datetime: new Date()
            }
        }
    }
</script>
