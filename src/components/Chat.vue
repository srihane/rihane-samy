<template lang="fr">
    

    <div id="chat-box" class="container">

        <div v-if="!joined">
            <div class="input-group mb-3">
                <input v-model="user" v-on:keyup.enter="userConnected()" type="text" class="form-control" placeholder="Pseudo" aria-label="Recipient's username" aria-describedby="basic-addon2">
                <span class="btn btn-primary" id="basic-addon2" v-on:click="userConnected()"><i class="fa-solid fa-arrow-right-to-bracket"></i></span>
            </div>
        </div>
    
        <div v-if="joined">
        <h3>Chat</h3>

            <div id="msg-box">
                <div v-for="msg in messages.slice().reverse()">
                    <p>[{{msg.date}}] {{msg.user}} : {{msg.text}}</p>
                </div>
            </div>
            <div class="input-group mb-3">
                <input v-model="text" v-on:keyup.enter="sendMessage()" type="text" class="form-control" placeholder="Message ..." aria-label="Recipient's username" aria-describedby="basic-addon2">
                <span class="btn btn-primary" id="basic-addon2" v-on:click="sendMessage()"><i class="fa-solid fa-paper-plane"></i></span>
            </div>
            <hr>
            <i class="fa-solid fa-user"></i> 
            <br />
            <br />
            <p v-for="us in users">{{us.user}}</p>

            <br />

            <!--{{messages}}-->
        </div>

    </div>

</template>

<script>
// Socket.io
import io from 'socket.io-client'


export default {
    name:"chat",
    data() {
        return {
            joined: false,
            user: "",
            data: {},
            users: [],
            messages: [],
            text: "",
        }
    },
    methods: {
        userConnected() {
            console.log("New user connected")
            this.socketInstance = io("http://localhost:3000")
            this.joined = true; 

                // Send the messages to the server
                this.socketInstance.emit('newconnected', this.user)
                
                this.socketInstance.on(
                    "newconnected", (data) => {
                        this.users = data
                        console.log(data)
                    }
                )
                

                    this.socketInstance.on(
                        "message:received", (data) => {
                            this.messages = this.messages.concat(data)
                        }
                    )
    
        },
        sendMessage() {
            this.addMessage();
            this.text = ""
        },
        addMessage() {

            const message = {
                date: new Date().getTime(),
                text: this.text,
                user: this.pseudo
            }

            // Add the new message to the list of messages
            this.messages = this.messages.concat(message)

            // Send the messages to the server
            this.socketInstance.emit('message', message)

        }
    }
}
</script>

<style>

#chat-box {
    width: 500px;
}

#msg-box {
    border: 1px solid lightgrey;
    height: 200px;
    border-radius: 5px 5px 0px 0px;
    overflow: auto;

    display: flex;
    flex-direction: column-reverse;
}

</style>