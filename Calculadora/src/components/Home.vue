<template>
    <div>
        <h4>Numero 1</h4>
        <input type="number" v-model="number.X" /><br />

        <input type="text" v-model="number.Operador" /><br />

        <h4>Numero 2</h4>
        <input type="number" v-model="number.Y" /><br />

        <button type="button" v-on:click="Operacion(number.X,number.Y,number.Operador)">
            Solución
        </button>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                number: {
                    X: ' ',
                    Y: ' ',
                    Operador: ' ',
                },
            }
        },
        methods: {
            Operacion(n1, n2, Operador) {
                var x = n1;
                var y = n2;
                var suma = parseFloat(x) + parseFloat(y);
                var resta = parseFloat(x) - parseFloat(y);
                var producto = parseFloat(x) * parseFloat(y);
                var division = parseFloat(x) / parseFloat(y);

                if (Operador == '+') {
                    alert('Operacion' + ' ' + suma)
                }
                else if (Operador == '-') {
                    alert('Operacion' + ' ' + resta)
                }
                else if (Operador == '*') {
                    alert('Operacion' + ' ' + producto)
                }
                else if (Operador == '/') {
                    alert('Operacion' + ' ' + division)
                }
            }
        }
    }
    
</script>

<style scoped>
    .number {
        background-color: lightskyblue;
        color: black;
    }
    .text {
        background-color: royalblue;
        color: black;
    }
    .button {
        background-color: mediumblue;
        color: whitesmoke;
    }
</style>
