<template>
    <div>
        <div className="h4 mt-4">Number of nodes to render:</div>
        <div className="my-2">
            <span className="me-3">
                <label>
                    <input 
                        type="number"
                        className="arena__input"
                        name="numberOfNodes"
                    > 
                </label>
            </span>
            <span className="btn btn-primary mb-1">
                BUILD
            </span>
        </div>
        <div className="arena p-3" id="arena">
        </div>
    </div>
</template>

<script>

export default {
    name: 'NodeArena',
    components: {},
    data  () {
        return {
            numberOfNodes: 0,
            nodes: []
        }
    },
    methods: {
        generateRandomNumber(min, max) {
            return Math.floor(Math.random() * (max - min + 1) + min);
        },
        buildNodeMap() {
            const arena = document.getElementById("arena").getBoundingClientRect();
            const newNodes = [];
            for (let i = 0; i < this.numberOfNodes; i++) {
                newNodes.push({
                    x: this.generateRandomNumber(36, arena.width - 36),
                    y: this.generateRandomNumber(136, arena.height + 36),
                    color: `rgb(${this.generateRandomNumber(0, 255)}, ${this.generateRandomNumber(0, 255)}, ${this.generateRandomNumber(0, 255)})`,
                    id: i
                });
            }
            this.nodes = newNodes
        }
    }
}
</script>

<style>
.arena {
    height: calc(100vh - 148px);
    width: calc(100vw - 48px);
    margin: 24px;
    background-color: rgba(68, 0, 255, 0.151);
    box-shadow: 0px 0px 15px 5px rgb(156, 156, 156);
}

.arena__input {
    font-size: 20px;
    width: 64px;
}
</style>
