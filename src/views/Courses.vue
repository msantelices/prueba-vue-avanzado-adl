<template>
    <v-container>
        <h1 class="my-3 text-center">Lista de cursos</h1>
        <v-row>
            <v-col cols="4" v-for="(course, index) in courses" :key="index">
                <v-card>
                    <v-img
                    height="200px"
                    src="https://cdn.pixabay.com/photo/2020/07/12/07/47/bee-5396362_1280.jpg"
                    >
                    </v-img>
                    <div class="m-5">
                        Javascript Avanzado 
                    </div>

                    <v-card-text>
                        <div class="font-weight-bold ml-8 mb-2">
                            Información
                        </div>

                        <v-timeline
                            align-top
                            dense
                        >
                            <v-timeline-item
                            v-for="message in messages"
                            :key="message.time"
                            :color="message.color"
                            small
                            >
                            <div>
                                <div class="font-weight-normal">
                                <strong>{{ message.from }}</strong> @{{ message.time }}
                                </div>
                                <div>{{ message.message }}</div>
                            </div>
                            </v-timeline-item>
                        </v-timeline>
                    </v-card-text>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
</template>
<script>

export default {
    data(){
        return{
        "messages": [
                        {
                        from: 'You',
                        message: `Sure, I'll see you later.`,
                        time: '10:42am',
                        color: 'deep-purple lighten-1',
                        },
                        {
                        from: 'John Doe',
                        message: 'Yeah, sure. Does 1:00pm work?',
                        time: '10:37am',
                        color: 'green',
                        },
                        {
                        from: 'You',
                        message: 'Did you still want to grab lunch today?',
                        time: '9:47am',
                        color: 'deep-purple lighten-1',
                        },
                    ],
        "courses": [1,2,3,4]
        }
    }
}
</script>
