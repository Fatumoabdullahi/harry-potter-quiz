# harry-potter-quiz
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Times New Roman', Times, serif;
}

body{
    background: coral;
}

.start_btn{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}

.rules_box, .quiz_box, .result-page{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    box-shadow: 0px 4px 8px 0 rgba(0,0,0,0.2)
                0px 6px 20px 0 rgba(0,0,0,0.19);
}

.rules_box.activeInfo{
    z-index: 5;
    opacity: 1;
    pointer-events: auto;
    transform: translate(-50%, -50%) scale(1);
}

.start_btn button{
    font-size: 25px;
    font-weight: 500;
    color: coral;
    padding: 15px 30px;
    outline: none;
    border: none;
    border-radius: 5px;
    background: white;
    cursor: pointer;
}

.rules_box{
    width: 540px;
    background:white;
    border-radius: 5px;
    opacity: 0;
    pointer-events: none;
    transform: translate(-50%, -50%) scale(0.9);
}

.rules_box .rules_title{
    height: 60px;
    width: 100%;
    border-bottom: 1px solid lightpink;
    display: flex;
    align-items: center;
    padding: 0 35px;
    font-size: 20px;
    font-weight: 600;   
}

.rules_box .rules_list{
    padding: 15px 35px;
}

.rules_box .rules_list .rules{
margin: 5px 0;
font-size: 15px;
}

.rules_box .rules_list .rules span{
    font-weight: 600;
    color: red;
}
.rules_box .buttons{
    height: 60px;
    display: flex;
    align-items: center;
    justify-content: flex-end;
    padding: 0 35px;
    border-top: 1px solid lightpink;
}

.rules_box .buttons button{
    margin: 0 5px;
    height: 40px;
    width: 100px;
    border: 1px solid lightpink;
    background: coral;
    border-radius: 5px;
    color: white;
    font-size: 15px;
    font-weight: 500;
    cursor: pointer;
    transition: all 0.3s ease;   
}
.buttons button .restart{
    color: white;
    background: coral;
}

.buttons button .restart:hover{
    background:;
}

.buttons button .quit{
    color: coral;
}

.buttons button .quit:hover{
    color: white;
    background: coral;
}
.quiz_box{
    width: 550px;
    background: white;
    border-radius: 5px;
    opacity: 0;
    pointer-events: none;
    transform: translate(-50%, -50%) scale(0.9);
}

.quiz_box header{
    position: relative;
    z-index: 99;
    height: 70px;
    padding: 0 30px;
    background: white;
    display: flex;
    align-items: center;
    justify-content: space-between;
    border-radius: 5px 5px 0 0;
    box-shadow: 0px 3px 5px 1px rgba(0,0,0,0.3);
}

.quiz_box header .title{
    font-size: 20px;
    font-weight: 600;
}

.quiz_box header .timer{
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 195px;
    height: 45px;
    background: coral;
    border: 1px solid lightpink;
    border-radius: 5px;
    padding: 0 8px;
}

.quiz_box header .timer .time_text{
    font-weight: 400;
    font-size: 17px;
    user-select: none;
}

.quiz_box header .timer .timer_second{
    font-size: 18px;
    font-weight: 500;
    background: #343a40;
    height: 30px;
    width: 45px;
    color: #fff;
    text-align: center;
    line-height: 30px;
    border-radius: 5px;
    border: 1px solid #343a40;
    user-select: none;
}
.quiz_box section{
    padding: 25px 30px 20px 30px;
}

.quiz_box section .question_text{
    font-size: 25px;
    font-weight: 600;
}
.quiz_box section .option-list{
    padding: 20px 0;
    display: block;
}
section .option-list .options{
    background: lightpink;
    border: 1px solid rgb(247, 214, 165);
    border-radius: 5px;
    padding: 8px 15px;
    margin-bottom: 15px;
    font-size: 17px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    cursor: pointer;
}

section .option-list .options:hover{
    color: coral;
    background: white;
    border-color: #b8daff;
}

.option-list .options:last-child{
    margin-bottom: 0px;
}

.option-list .options .icon{
    height: 26px;
    width: 26px;
    border: 2px solid transparent;
    border-radius: 50%;
    text-align: center;
    font-size: 13px;
    line-height: 24px;
    pointer-events: none;
}
.option-list .options .icon.tick{
color: #3fa356;
border-color: #3e9e54;
} 

.quiz_box footer{
    height: 60px;
    width: 100%;
    padding: 0 30px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.quiz_box footer .total_questions span{
    display: flex;
    user-select: none;
}

.quiz_box footer .total_questions span p{
    font-weight: 500;
}

.total_questions span p{
    padding-left: 0px;
    padding-right: 5px;
}


footer .next_button{
    height: 40px;
    padding: 0 13px;
    font-size: 18px;
    font-weight: 400;
    border: none;
    outline: none;
    color: white;
    background: coral;
    border-radius: 5px;
    border: 1px solid coral;
    cursor: pointer;
    transition: all 0.3s ease;
}
    
footer .next_button:hover{
    background:grey;
}

.result-page{
    background: white;
    width: 450px;
    padding: 25px 30px;
    border-radius: 5px;
    display: flex;
    text-align: center;
    align-items: center;
    flex-direction: column;
    justify-content: space-between;
    opacity: 0;
    pointer-events: none;
    transform: translate(-50%, -50%) scale(0.9);
}

.result-page .complete-text{
    font-size: 20px;
    font-weight: 500;
}

.result-page .score-text span{
    display: flex;
    margin: 10px 0;
    font-size: 18px;
    font-weight: 500;
}

.result-page .score-text span p{
    font-weight: 600;
    padding: 0 4px;
}

.result-page .buttons{
    display: flex;
    margin: 20px 0;
}

.result-page .buttons button{
    margin: 0 10px;
    height: 45px;
    padding: 0 20px;
    border: none;
    outline: none;
    font-size: 18px;
    font-weight: 500;
    border-radius: 5px;
    border: 1px solid coral;
    cursor: pointer;
}