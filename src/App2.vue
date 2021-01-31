<template>
    <div id="app">
        <div class="content">
            <div class="chat-container">
                <Chat v-if="visible"
                      :participants="participants"
                      :myself="myself"
                      :messages="messages"
                      :chat-title="chatTitle"
                      :placeholder="placeholder"
                      :colors="colors"
                      :border-style="borderStyle"
                      :hide-close-button="hideCloseButton"
                      :close-button-icon-size="closeButtonIconSize"
                      :submit-icon-size="submitIconSize"
                      :submit-image-icon-size="submitImageIconSize"
                      :load-more-messages="toLoad.length > 0 ? loadMoreMessages : null"
                      :async-mode="asyncMode"
                      :scroll-bottom="scrollBottom"
                      :display-header="true"
                      :send-images="true"
                      :profile-picture-config="profilePictureConfig"
                      :timestamp-config="timestampConfig"
                      :link-options="linkOptions"
                      :accept-image-types="'.png, .jpeg'"
                      @onImageClicked="onImageClicked"
                      @onImageSelected="onImageSelected"
                      @onMessageSubmit="onMessageSubmit"
                      @onType="onType"
                      @onClose="onClose('param value')"/>
            </div>
            <v-card
            class="mx-auto"
            max-width="344"
            tile
            colour="Primary"
            >
            <v-card-text>
                <v-img
                max-height="150"
                max-width="250"
                src="@/assets/avatar3.png"
                ></v-img>
                <p class="display-1 text--primary">
                    Linda Brown (Client)
                </p>
                <div class="text--primary">
                    Frozen Food Shop Owner<br>
                    10 shops - 100 staff<br>
                    <br><br>
                </div>
            </v-card-text>
            </v-card>
            <v-card
            class="mx-auto"
            max-width="344"
            tile
            colour="Primary"
            >
            <v-card-text>
                <div></div>
                <p class="display-1 text--primary">
                    John Smith (Freelancer)
                </p>
                <div class="text--primary">
                    3 years web developer<br>
                    The Hong Kong Polytechnic University<br>
                    React - Firebase - Adobe - Creative Cloud<br>
                    Audocad - Photoshop - Java - MySQL<br>
                    <br><br>
                </div>
                <div>
                </div>
                <v-btn block>
                    Accept
                </v-btn>
                <br><br>
                <v-btn block>
                    Reject
                </v-btn>
            </v-card-text>
            </v-card>
        </div>
    </div>
</template>

<script>
    import Chat from './components/Chat.vue'

    export default {
        name: 'app',
        components: {
            Chat
        },
        data() {
            return {
                visible: true,
                participants: [
                    {
                        name: 'John Smith',
                        id: 1,
                        profilePicture: ''
                    },
                ],
                myself: {
                    name: 'Linda Brown',
                    id: 3,
                    profilePicture: ''
                },
                messages: [
                ],
                chatTitle: 'Linda and John',
                placeholder: 'send your message',
                colors: {
                    header: {
                        bg: '#d30303',
                        text: '#fff'
                    },
                    message: {
                        myself: {
                            bg: '#fff',
                            text: '#525252'
                        },
                        others: {
                            bg: '#fb4141',
                            text: '#fff'
                        },
                        messagesDisplay: {
                            //bg: 'rgb(247, 243, 243)',
                            //bg: '#f7f3f3'
                            bg: '#f7f3f3'
                        }
                    },
                    submitIcon: '#b91010',
                    submitImageIcon: '#b91010',
                },
                borderStyle: {
                    topLeft: "10px",
                    topRight: "10px",
                    bottomLeft: "10px",
                    bottomRight: "10px",
                },
                hideCloseButton: false,
                submitIconSize: 24,
                submitImageIconSize: 24,
                closeButtonIconSize: "20px",
                asyncMode: true,
                toLoad: [
                    {
                       content: "Hi, John! I would like you to help me with building an e-commerce platform.",
                        participantId: 3,
                        timestamp: { year: 2016, month: 3, day: 5, hour: 10, minute: 10, second: 3, millisecond: 123 },
                        uploaded: true,
                        viewed: true
                    },
                    {
                        content: "Sure! I can see your requirements, I definitely can help.",
                        participantId: 1,
                        timestamp: { year: 2016, month: 1, day: 5, hour: 19, minute: 10, second: 3, millisecond:123 },
                        uploaded: true,
                        viewed: true
                    },
                    {
                        content: "I will offer HKD20000 if you make it.",
                        participantId: 3,
                        timestamp: {year: 2012, month: 3, day: 5, hour: 20, minute: 10, second: 3, millisecond: 123},
                        uploaded: true,
                        viewed: true,
                        type: 'text'
                    },
                ],
                scrollBottom: {
                    messageSent: true,
                    messageReceived: false
                },
                profilePictureConfig: {
                    others: true,
                    myself: true,
                    styles: {
                        width: '30px',
                        height: '30px',
                        borderRadius: '50%'
                    }
                },
                timestampConfig: {
                    format: 'HH:mm',
                    relative: false
                },
                // there are other options, you can check them here
                // https://soapbox.github.io/linkifyjs/docs/options.html
                linkOptions: {
                    myself: {
                        className: 'myLinkClass',
                        events: {
                            click: function (e) {
                                alert('Link clicked!');
                            },
                            mouseover: function (e) {
                                alert('Link hovered!');
                            }
                        },
                        format: function (value, type) {
                            if (type === 'url' && value.length > 50) {
                                value = value.slice(0, 50) + '…';
                            }
                            return value;
                        }
                    },
                    others: {
                        className: 'othersLinkClass',
                        events: {
                            click: function (e) {
                                alert('Link clicked!');
                            },
                            mouseover: function (e) {
                                alert('Link hovered!');
                            }
                        },
                        format: function (value, type) {
                            if (type === 'url' && value.length > 50) {
                                value = value.slice(0, 50) + '…';
                            }
                            return value;
                        }
                    }
                }
            }
        },
        methods: {
            // eslint-disable-next-line
            onType: function (e) {
                // eslint-disable-next-line
                console.log('typing');
            },
            loadMoreMessages(resolve) {
                setTimeout(() => {
                    resolve(this.toLoad);
                    //Make sure the loaded messages are also added to our local messages copy or they will be lost
                    this.messages.unshift(...this.toLoad);
                    this.toLoad = [];
                }, 1000);
            },
            onMessageSubmit(message) {
                /*
                * example simulating an upload callback.
                * It's important to notice that even when your message wasn't send
                * yet to the server you have to add the message into the array
                */
                this.messages.push(message);

                /*
                * you can update message state after the server response
                */
                // timeout simulating the request
                setTimeout(() => {
                    message.uploaded = true
                    message.viewed = true
                }, 2000)
            },
            onClose(param) {
                console.log(param)
                this.visible = false;
            },
            addMessage() {
                /* this.messages.push(
                    {
                        content: "Update state",
                        // myself: false,
                        participantId: 1,
                        timestamp: {year: 2014, month: 3, day: 5, hour: 20, minute: 10, second: 3, millisecond: 123},
                        uploaded: true,
                        viewed: true
                    }
                ) */
                this.messages.push(
                    {
                        type: 'image',
                        preview: null,
                        src: 'https://pbs.twimg.com/profile_images/875996174305472512/upM71pVR.jpg',
                        content: 'image',
                        participantId: 1,
                        timestamp: {year: 2014, month: 3, day: 5, hour: 20, minute: 10, second: 3, millisecond: 123},
                        uploaded: true,
                        viewed: false
                    }
                )
            },
            onImageSelected({file, message}){
                let src = 'https://pbs.twimg.com/profile_images/875996174305472512/upM71pVR.jpg'
                this.messages.push(message);
                /**
                 * This timeout simulates a requisition that uploads the image file to the server.
                 * It's up to you implement the request and deal with the response in order to
                 * update the message status and the message URL
                 */
                setTimeout((res) => {
                    message.uploaded = true
                    message.src = res.src
                }, 3000, {src});
            },
            onImageClicked(message){
                /**
                 * This is the callback function that is going to be executed when some image is clicked.
                 * You can add your code here to do whatever you need with the image clicked. A common situation is to display the image clicked in full screen.
                 */
                console.log('Image clicked', message.src)
            }
        }
    }
</script>

<style>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }

    .content {
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: space-evenly;
        flex-wrap: wrap;
    }

    .chat-container {
        display: flex;
        align-items: center;
        justify-content: center;
        background: rgb(247, 243, 243);
        padding: 10px 0 10px 0;
        height: 500px;
        width: 350px;
    }

    .external-controller {
        background: #2c3e50;
        height: 300px;
        width: 600px;
        display: flex;
        color: #eee;
    }

    .controller-btn-container {
        display: flex;
        justify-content: center;
        align-items: center;
        padding-left: 20px;
        padding-right: 20px;
        flex-wrap: wrap;
    }

    .btn-message {
        cursor: pointer;
        background: #eee;
        border: none;
        height: 40px;
        color: #2c3e50;
        border-radius: 5px;
        outline: none;
        transition: 0.3s;
    }

    .btn-participant {
        cursor: pointer;
        background: #eee;
        border: none;
        height: 40px;
        color: #2c3e50;
        border-radius: 5px;
        outline: none;
        transition: 0.3s;
    }

    .btn-message:hover {
        background: rgb(255, 255, 255);
    }

</style>
