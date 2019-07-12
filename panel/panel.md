nodejs 服务端代码
```js
//bandwagon-banel搬瓦工信
router.get('/kiwi',async ctx=>{

        //这里的id换成你自己的id，key换成你自己的key
        const id = '';
        const key = '';
        //console.log("kiwi");
        try {
                await   rp('https://api.64clouds.com/v1/getLiveServiceInfo?veid='+id+'&api_key='+key).then(res=>{
                        ctx.body = {res};
                }).catch(e=>{
                        ctx.body = {msg:'error'};
                });
        } catch(e) {
                ctx.body = {msg:'error'};
        }
})
```

