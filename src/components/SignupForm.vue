<template>
    <form>
        <label>Email:</label>
        <input type="email" name="email" required v-model="email" />

        <label>Password:</label>
        <input type="email" name="password" required v-model="password"/>

        <label>Role:</label>
        <select v-model="role">
            <option value="developer">Web developer</option>
            <option value="designer">Designer</option>
            <option value="tester">QA tester</option>
        </select>

        <div class="terms">
            <input type="checkbox" v-model="terms" />
            <label>Please accept terms and agreement</label>
        </div>

        <div class="">
            <input type="checkbox" value="mark" v-model="names" />
            <label>Mark</label>
        </div>

        <div class="terms">
            <input type="checkbox" value="dexter" v-model="names" />
            <label>Dexter</label>
        </div>

        <div class="terms">
            <input type="checkbox" value="abs" v-model="names" />
            <label>Abs</label>
        </div>
    </form>
</template>

<script>
export default {
    data() {
        return {
            email: '',
            password: '',
            role: '',
            terms: false,
            names:[],
        }
    },
    watch: {
        names(newValue, oldValue) {
            console.log('Updated names:', newValue);
        }
    }
}
</script>

<style scoped>
    form {
        padding: 5rem 4rem;
        background: #fff;
        border-radius: 25px;
        box-shadow: 1px 2px 2px #fff;
        width: 400px;
        display: flex;
        align-items: start;
        justify-content: center;
        flex-direction: column;
        gap: 0.5em;
    }

    label {
        display: inline-block;
        font-family: Consolas;
        font-weight: 800;
    }

    input, select {
        box-sizing: border-box;
        padding: 0.4rem 0.6rem;
        width: 100%;
        border: none;
        border-bottom: 1px solid #ccc;
    }

    option {
        padding: 0.3em 0.2em;
        margin: 2px;
    }

    input[type='checkbox'] {
        display: inline-block;
        width: 16px;
        margin: 0 10px 0 0;
        position: relative;
        top: 2;
    }

    .terms {
        margin: 2rem 0 0 0;
    }
</style>