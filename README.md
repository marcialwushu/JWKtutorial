# JWKtutorial

Crie jwk para criar e verificar JWT. O tutorial também demonstra como usar a biblioteca node-jose para criar e verificar JWT da JWK.

## Passo 1: Crie duas chaves privadas como:

```
openssl genrsa -out k1.private 1024
openssl genrsa -out k2.private 1024
```

## Passo 2: Executar o aplicativo


```
npm start
```

## Resultado 

```json

> jwk@1.0.0 start C:\Users\user\Documents\Workspace\GITHUB\JWK
> node index.js

public jwk ::  {"keys":[{"kty":"RSA","kid":"aH3RVlGGZ6GWrtAyjz5YR7ZhX7Zowy1hvRrqM60O97o","n":"tGNVhtRo07AVt1p1HxPPWUgYPQY0HES0kROUPYk3IBDp4-YkU-uVUMR5ACppm1e0Lg26MYDEISoU7JsmHWW_xe5McAMY9hblBEeOwcvf9yCsLyDL-S7R_7Ap2tjNu98E45F-HohjGKc6eUKIyVlMmfrCeBoNZjoSH4Nk9VGP9ck","e":"AQAB"},{"kty":"RSA","kid":"uiSybdIDRErTGWLqGEm9XlKeMjYn5jcjZWQ5Pd6fCMY","n":"vyHJxbaNmWeryJuqLIrFs69qQo1M7vXA8CzrOffSjo7bowTRFGMCXltG0UURRPy4fzjoqcTZz-Fs9C_nQG5pzXz2txLHa1SJtufWBtsxn8CLoCrfKWjTaFl0-7F4Hxht3MyTVqUj6vmTvoZB6YWnNYXIBUOMdS4Sid0IGIR-HR0","e":"AQAB"}]}


private jwk ::  {"keys":[{"kty":"RSA","kid":"aH3RVlGGZ6GWrtAyjz5YR7ZhX7Zowy1hvRrqM60O97o","n":"tGNVhtRo07AVt1p1HxPPWUgYPQY0HES0kROUPYk3IBDp4-YkU-uVUMR5ACppm1e0Lg26MYDEISoU7JsmHWW_xe5McAMY9hblBEeOwcvf9yCsLyDL-S7R_7Ap2tjNu98E45F-HohjGKc6eUKIyVlMmfrCeBoNZjoSH4Nk9VGP9ck","e":"AQAB","d":"qD0Y8GY82moY5ufb4j80nL1rtcaKZW8CxWfwUzAdlK-RpHbpnMdUfH6xp6Dm2_YBWw58gFzrD09TMpVFCBf0sZDuLo4T0oGAm0ENjiay0q-Gi5028jKXu2JUVlOENRqW_RjVerVAyapZRSQdjWg5mE8oCDo_N1rS3wm2utdj2b0","p":"5UM6YedxICODKNi7Wr7Xoz0oR2K0ShjiRdl4Wl9uRxU7wfUhJJLIRuIMME1b7sIlrNIogfxk_QmBiJsgj43N_w","q":"yWztFm8sLN4w3q1iRvUupEZZgYJvSxW55bw7-qYSU3hTD8j4ycEZKnngMmqH39vPMOquJbmBSmSwRYZksQ9MNw","dp":"PhRQMMaM2VkEYQEe6lmW5nre90WA8DeAvc0_S6lfoRvczI5l5RNh69-10TaBWEt2DC_0DA6eAe6bBrSKwpRxXQ","dq":"wQETqLR8Ar4g264Nhmp298fFChi-pZa62wxj-Ida9gpMpMpwwXm6sH25uvVjHriTro6gsdsvrOYQFX5yS0qaPw","qi":"Ld5D9EB-EDOFC5BWNc5PfUduSggBfXSJaOpVvcCOSHeez5LAM5FfnU6tfGg9z-w_01-X1gmiXHfv-NaRxm-h1A"},{"kty":"RSA","kid":"uiSybdIDRErTGWLqGEm9XlKeMjYn5jcjZWQ5Pd6fCMY","n":"vyHJxbaNmWeryJuqLIrFs69qQo1M7vXA8CzrOffSjo7bowTRFGMCXltG0UURRPy4fzjoqcTZz-Fs9C_nQG5pzXz2txLHa1SJtufWBtsxn8CLoCrfKWjTaFl0-7F4Hxht3MyTVqUj6vmTvoZB6YWnNYXIBUOMdS4Sid0IGIR-HR0","e":"AQAB","d":"NVmEDYjwK1Kxs3Qn4vj1SDt9aIgyYjz8ls2i9vJCtoIPsogkqBEe1yGZOc6SjHQSN4i2ALUuqwTcOaipXuWy6Cl9KaSFYEp3heP_x3QtLBkwHmi3hqaEHK8QLUNWTXeE5OsZD6NdmWdnnnzMPqg9UlJjoAnL9XCutjNShyHAR20","p":"9df4iGGwl-OxBCr6IngCWveIDMgo7RljxamFwoX88JZjO13Kcm9PuJDc9vwoKYjiMrabkHdI3RRDV-HaMINofw","q":"xwcwmX9CBfCfTYpk9QEYMVy853h0M95bzVd_kX9FGioCA1HrBLBB5kVl6cAL1NWsLduK2K-OaIeeToFFVdlMYw","dp":"NL_oderwJ0cVvl0yWp8Bcl9Wc9em4GjoPYtIRhrV0RGTrTNMsw0rP-DlaKFmRLM4RcVkz7Soj7c_U-YEGRC5JQ","dq":"L0_DOsnojPbtN4aNhzxSXvGXqkKVBPt3wTFqjtC9QYH45ocjogKwN6gJmO5hIaAFhQUqVWYuKSUL-cd7DvRP1w","qi":"xfMuIMnj2riITb_r4OmuLHCUUzw_43xBW-GK0KKTexWub2ZqeNM4lrzhI1ZaPZli3TAQix-Qj8I_UFxF3lSHFg"}]}     


token ::  eyJhbGciOiJSUzI1NiIsImtpZCI6ImFIM1JWbEdHWjZHV3J0QXlqejVZUjdaaFg3Wm93eTFodlJycU02ME85N28ifQ.eyJtc2ciOiJIZWxsbyEifQ.Y0h4KUax_qCzqZqJe5uUTbFC5g5Ym1SGZqXtPJ3Mn2e1GHwEcYTcum5ggCtkZ7fRjvy6yUk-sRMoSDzPVRq3o20wC56AWFiZW8VPCBiaUZAQzKf6Kgprg8ShwsTOZsDZCwRm_-FBxuDmXvvF7iOl6z4YZp_JC5OcaqFFcp_MF7o


payload ::  {"msg":"Hello!"}
```

