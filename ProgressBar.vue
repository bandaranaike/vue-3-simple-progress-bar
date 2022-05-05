<template>
    <div class="progress">
        <div
            :style="`--color: ${color}; --height: ${height}px; width:${currentValue}%`"
            class="progress-bar progress-bar-striped progress-bar-animated"
            role="progressbar"
            :aria-valuenow="currentValue"
            aria-valuemin="0"
            aria-valuemax="100"
            :title="`${currentValue}%`"
            :class="{'animated-bg': animation, 'striped-bg':strip}"
        >
        </div>
    </div>
</template>

<script>
export default {
    name: "ProgressBar"
}
</script>

<script setup>
defineProps({
    color: {
        default: "#17a2b8"
    },
    height: {
        default: 16,
        type: Number
    },
    currentValue: {
        default: 20,
        type: Number
    },
    animation: {
        default: true
    },
    strip: {
        default: true
    }
})
</script>

<style scoped>
@keyframes progress-bar-stripes {
    from {
        background-position: 1rem 0;
    }
    to {
        background-position: 0 0;
    }
}

.striped-bg {
    background-image: linear-gradient(45deg, rgba(255, 255, 255, .15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, .15) 50%, rgba(255, 255, 255, .15) 75%, transparent 75%, transparent);
    background-size: 1rem 1rem;
}

.animated-bg {
    -webkit-animation: progress-bar-stripes 1s linear infinite;
    animation: progress-bar-stripes 1s linear infinite;
}

.progress-bar {
    --color: #ff6c00;
    --height: 16;
    display: flex;
    flex-direction: column;
    justify-content: center;
    color: #fff;
    text-align: center;
    background-color: var(--color);
    transition: width .6s ease;
    height: var(--height);
}

.progress {
    display: flex;
    overflow: hidden;
    font-size: .75rem;
    background-color: #e9ecef;
    border-radius: .25rem;
}

</style>
