
<template>
    <div class="w-full z-0 bg-zinc-900 section h-content" >
        <div class="pt-16 md:pt-40 pb-8 md:pb-20 max-w-7xl mx-auto text-6xl md:text-8xl text-white text-center">
            <div class="opacity-70 text-2xl  md:text-5xl font-semibold md:font-bold tracking-tight pb-1 md:pb-6">ZeroPage Angels Camp 2022</div>
            <vue-typer
                :text='[
                "Do whatever you want",
                "ZP의 3번째 정규행사",
                "ZP가 모여 펼치는 코딩 축제"
                ]'
                :repeat='Infinity'
                :shuffle='false'
                initial-action='typing'
                :pre-type-delay='70'
                :type-delay='70'
                :pre-erase-delay='2000'
                :erase-delay='300'
                erase-style='clear'
                :erase-on-complete='false'
                caret-animation='blink'
                class="gradient-one md:pt-20 font-extrabold tracking-tight md:text-8xl text-4xl"
            ></vue-typer>
            <div class="pt-4 md:pt-8 font-medium text-white text-xl md:text-3xl ">11월 11일 19시 | 서울 마포구 동교로 156-12 2층</div>


        </div>
        <div class="max-w-4xl mx-auto pb-20 pt-4" style="text-align:center">
            <a href="" target="blank" class="button1">신청하기</a>
        </div>

        

        <div class="max-w-7xl mx-auto text-3xl md:text-4xl pt-16 mt-10 text-white mb-10 md:mb-14 font-medium px-6 md:px-10 text-center">About</div>
        <div class="max-w-7xl mx-auto px-6 md:px-10">
            <div class="grid grid-cols-1 sm:grid-cols-1 md:grid-cols-3 gap-x-8 gap-y-6 pb-16 md:pb-24 px-8 ">
                <div class="h-content">
                    <div class="text-xl md:text-2xl text-white font-semibold mb-2 md:mb-3">Who</div>
                    <div class="text-base md:text-lg text-slate-400 keep-all">ZeroPage 회원이라면 누구나 참석 가능합니다! </div>
                </div>
                <div class="h-content">
                    <div class="text-xl md:text-2xl text-white font-semibold mb-2 md:mb-3">When & Where</div>
                    <div class="text-base md:text-lg text-slate-400 keep-all">11월 11일 19시 </br>서울 마포구 동교로 156-12 2층</div>
                </div>
                <div class="h-content">
                    <div class="text-xl md:text-2xl text-white font-semibold mb-2 md:mb-3">What</div>
                    <div class="text-base md:text-lg text-slate-400 keep-all">평소에 아디이어가 떠올라서 만들었으면 좋겠다라는 생각은 했으나 바쁘다고, 혹은 어렵다고 하지 못 했던 것들을 공부하고 만드는 자리입니다. </div>
                </div>
            </div>
        </div>

        <!-- <div class="max-w-7xl mx-auto pb-14 px-6 md:px-10 ">
            <div class="max-w-7xl mx-auto text-3xl md:text-4xl pt-10 mt-20 text-white mb-10 md:mb-14 font-medium px-6 md:px-10 text-center">Conference</div>
            <div class="mx-auto grid sm:grid-cols-1 md:grid-cols-3 gap-x-4 gap-y-6 pb-16 md:pb-24 items-start">
                <Card1 class="mx-auto w-100 md:w-100" />
                <Card2 class="mx-auto w-100 md:w-100" />
                <Card3 class="mx-auto w-100 md:w-100" />
            </div>
            
        </div> -->

        <div class="max-w-7xl mx-auto text-2xl pt-20 pb-20 md:text-3xl text-white font-medium px-6 md:px-10 text-center ">
            <a href="https://wiki.zeropage.org/wiki.php/AngelsCamp/2022" class="hover:underline" target="blank">더 많은 정보가 궁금하신가요?</a>
        </div>
        
    </div>

    
</template>

<script>

</script>

<style scoped>
.gradient-one{
  color: #79c0ff;
  background: linear-gradient(92.7deg,#32bf61 -1.37%,#3f64f7 90%);
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
}
.keep-all{
  word-break: keep-all;
}
.button1{
  text-align: center;
  padding-left: 100px;
  padding-right: 100px;
  padding-top: 20px;
  padding-bottom: 20px;
  background: #3f64f7;
  color: white;
  font-size: 16pt;
  font-weight: bold;
  border-radius: 10px;
}
.button1:hover{
  text-align: center;
  padding-left: 100px;
  padding-right: 100px;
  padding-top: 20px;
  padding-bottom: 20px;
  border: 1px solid #3f64f7;
  background: white;
  color:#3f64f7;
  font-size: 16pt;
  font-weight: bold;
  border-radius: 10px;
}

>>> .vue-typer .custom.char.selected {
  @apply bg-blue-400 text-white;
}
</style>