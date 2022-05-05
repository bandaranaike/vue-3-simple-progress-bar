# Vue 3 Simple Progress Bar

This is a light-weight simple progress bar with minimum variations. Design for Vue 3.

### Attributes

| Name            | Type    | Default Value | Description                        |
|-----------------|---------|---------------|------------------------------------|
| `color`         | String  | #17a2b8       | Ex: red, #ddddd, rgb(255, 120, 45) |
| `height`        | Number  | 16            | Converts to pixel(px)              |
| `current-value` | Number  | 20            | Range is 0-100                     |
| `animation`     | Boolean | true          | To animate, strip must be `true`   |
| `strip`         | Boolean | true          |                                    |

*Note : The progress bar takes parent container width.*

### Install

`npm install vue-3-simple-progress-bar`

### Usage

    <template>
        <div style="width:40%">
            <progress-bar></progress-bar>
        </div>
        <div style="width:40%; margin-top:20px">
            <progress-bar current-value="50" height="5" color="#3eb750" :strip="true" :animation="false"></progress-bar>
        </div>
    </template>

    <script setup>
    import ProgressBar from "vue3-simple-progress";
    
    </script>