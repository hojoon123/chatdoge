# chatdoge
변경하실 부분! 핵심사항입니다!

//오픈ai api에서 apikey를 받은뒤 apiKey 변수에 넣어주시면 됩니다.

//CORS 이슈 해결
//express로 cors 요청을 쉽게 받습니다. origin은 본인의 도메인 주소를 입력하셔야 합니다.
let corsOptions = {
    origin: "프론트도메인주소",
    credentials: true,
    optionsSuccessStatus: 30000,
}
app.use(cors(corsOptions));

//fetch 요청은 직접 작성하시면 됩니다.
const response = await fetch('백엔드서버의도메인주소/post요청주소', {
    method: 'POST',
    headers: {
        'Content-Type': 'application/json'
    },
    body: JSON.stringify({
        myDateTime: myDateTime,
        userMessages: userMessages,
        assistantMessages: assistantMessages,
    })
});
