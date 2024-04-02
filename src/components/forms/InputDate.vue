<template>
    <div class="floating-label">
        <input
            class="floating-input"
            type="text"
            onclick="(this.type='date')"
            placeholder=" "
        />
        <span class="highlight"></span>
        <label>{{ label }}</label>
    </div>
</template>

<script>
export default {
    props: {
        label: { required: true, type: String },
    },
};
</script>

<style lang="scss">
.floating-label {
    position: relative;
    margin-bottom: 2rem;
}

.floating-input {
    font-size: 1.6rem;
    padding: 1.2rem;
    display: block;
    width: 100%;
    background-color: transparent;
    border: 0.1rem solid #c3cdc9;
    border-radius: 0.4rem;
    color: #00291b;

    &:focus {
        outline: none;
    }
}

label {
    color: #999;
    font-size: 1.6rem;
    font-weight: normal;
    position: absolute;
    pointer-events: none;
    left: 12px;
    top: 9px;
    background-color: #fff;
    transition: 0.2s ease all;
    -moz-transition: 0.2s ease all;
    -webkit-transition: 0.2s ease all;
    padding: 0 0.5rem;
}

.floating-input:focus ~ label,
.floating-input:not(:placeholder-shown) ~ label {
    top: -1rem;
    font-size: 12px;
    color: #879a94;
}

.highlight {
    position: absolute;
    height: 50%;
    width: 100%;
    top: 15%;
    left: 0;
    pointer-events: none;
    opacity: 0.5;
}

.floating-input:focus ~ .highlight {
    -webkit-animation: inputHighlighter 0.3s ease;
    -moz-animation: inputHighlighter 0.3s ease;
    animation: inputHighlighter 0.3s ease;
}

/* animation */
@-webkit-keyframes inputHighlighter {
    from {
        background: #5264ae;
    }
    to {
        width: 0;
        background: transparent;
    }
}
@-moz-keyframes inputHighlighter {
    from {
        background: #5264ae;
    }
    to {
        width: 0;
        background: transparent;
    }
}
@keyframes inputHighlighter {
    from {
        background: #5264ae;
    }
    to {
        width: 0;
        background: transparent;
    }
}
</style>
