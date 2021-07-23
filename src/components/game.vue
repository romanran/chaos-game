<template>
    <div class="game">
        <div class="canvas-wrap" id="canvas"></div>
    </div>
</template>

<script>
import * as d3 from 'd3'
import { onMounted } from '@vue/runtime-core'
export default {
    setup() {
        let context
        const drawPoint = function(position, size = 3, color = '#80baa0') {
            context.fillStyle = color
            context.beginPath()
            context.arc(position.x, position.y, size, 0, 2 * Math.PI, true)
            context.fill()
        }
        onMounted(() => {
            const canvasWidth = 800
            const canvasHeight = 800
            const canvas = d3
                .select('#canvas')
                .append('canvas')
                .attr('width', canvasWidth)
                .attr('height', canvasHeight)
            context = canvas.node().getContext('2d')
            context.clearRect(0, 0, canvasWidth, canvasHeight)
            drawPoint({ x: 100, y: 600 })
        })
    }
}
</script>

<style>
.canvas-wrap canvas {
    border: 5px solid #50aa90;
    outline: 5px solid #80baa0;
}
</style>
