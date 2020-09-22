<template>
  <h1>HOME</h1>
</template>

<script>
import io from 'socket.io-client'

export default {
  name: 'Home',
  created () {
    const socket = io('https://140.124.71.226:3030')

    socket.on('connect', () => {
      socket.connected
        ? console.log('connected!')
        : console.log('connection failed!')

      console.log(socket)
    })
  }
}
</script>
