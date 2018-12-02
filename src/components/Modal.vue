<template>
    <div class="modal-mask">
        <div class="modal-wrapper">
            <div class="modal-container">
                <div class="headMenu">
                    <i class="far fa-star fa-lg"></i> <i class="fas fa-times fa-lg" @click="$emit('close')"></i>
                </div>

                <div class="icons">
                    <i class="fas fa-laptop fa-2x"></i>
                </div>
                <h4 class="title">
                    Utvecklare
                </h4>
                <div class="employer">
                   <i class="fas fa-globe"></i> ICA gruppen
                </div>
                <div class="location">
                   <i class="fas fa-map-marked-alt"></i> Stockholm
                </div>

                <div class="modal-header">
                    <i class="far fa-clock"></i> Heltid
                </div>

                <div class="modal-body">
                    <slot name="body">
                       <h3>Beskrivning:</h3>  
                       <p>Kunskaper:<br />- Python <br />- JavaScript <br />- Tidigare byggt RESTful HTTP API:s <br />- Kunskaper i NoSQL databaser. <br />- Van vidversionshanteringssystem som exempelvis git eller mercurial.</p>
                    </slot>
                </div>

                <div class="modal-footer">
                    <slot name="footer">
                        <p><strong>Kontakt:</strong> Per-Olof Vide, 08-01010110</p>
                        <div class="myButton"><i class="far fa-check-circle fa-lg"></i> Ansök</div>
                    </slot>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Modal"
    }
</script>

<style>
    .fa-star, .fa-times {
        cursor: pointer;
    }

    .fa-star:hover {
        font-weight: 900;
    }

    .modal-mask {
        position: fixed;
        z-index: 9998;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, .5);
        display: table;
        transition: opacity .3s ease;
    }

    .modal-wrapper {
        display: table-cell;
        vertical-align: middle;
    }

    .modal-container {
        width: 300px;
        margin: 0px auto;
        padding: 20px 30px;
        background-color: #fff;
        border-radius: 2px;
        box-shadow: 0 2px 8px rgba(0, 0, 0, .33);
        transition: all .3s ease;
    }

    .modal-header h3 {
        margin-top: 0;
        color: #42b983;
    }

    .modal-body {
        margin: 20px 0;
    }

    .modal-default-button {
        float: right;
    }

    .modal-enter {
        opacity: 0;
    }

    .modal-leave-active {
        opacity: 0;
    }
    .modal-enter .modal-container,
    .modal-leave-active .modal-container {
        -webkit-transform: scale(1.1);
        transform: scale(1.1);
    }

    .headMenu {
        display: flex;
        justify-content: space-between;

    }

.myButton {
	-moz-box-shadow:inset 0px 1px 0px 0px #9acc85;
    -webkit-box-shadow: inset 0px 1px 0px 0px #94de4e;
    box-shadow: inset 0px 1px 0px 0px #c9f5b8;
    background-color: #abff5c;
    border: 1px solid #96d858;
    display: inline-block;
    cursor: pointer;
    color: #0a0a0a;
    font-size: 13px;
    font-weight: bold;
    padding: 6px 12px;
    text-decoration: none;
}
.myButton:hover {
    background-color: #bdfa85;
}
.myButton:active {
	position:relative;
	top:1px;
}


</style>