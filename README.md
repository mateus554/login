<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>Login Page</title>
<style>
  body{font-family:Arial,sans-serif;background:#f5f6fa;display:flex;justify-content:center;align-items:center;height:100vh}
  .box{background:#fff;padding:30px;border-radius:15px;box-shadow:0 0 10px #0001;width:320px;text-align:center}
  input,button{width:100%;padding:10px;margin:8px 0;border:1px solid #ccc;border-radius:8px}
  button{background:#4f46e5;color:#fff;border:0;font-weight:bold;cursor:pointer}
  button:hover{background:#4338ca}
  .links{margin-top:10px;font-size:13px}
  .social{margin-top:20px}
  .btn{display:flex;align-items:center;justify-content:center;gap:10px;width:100%;padding:10px;margin-top:8px;border-radius:8px;font-weight:bold;border:0;cursor:not-allowed}
  .fb{background:#1877f2;color:#fff}
  .gg{background:#fff;color:#1877f2;border:1px solid #1877f2;cursor:not-allowed}
  .btn img{width:20px;height:20px}
  #eye{position:absolute;right:10px;top:50%;transform:translateY(-50%);cursor:pointer}
</style>
</head>
<body>
  <div class="box">
    <h2>Login</h2><p style="color:gray;font-size:14px">Welcome back</p>
    <input id="u" placeholder="Usuário/Email">
    <div style="position:relative">
      <input type="password" id="p" placeholder="Senha"><span id="eye">👁️</span>
    </div>
    <div class="links"><a href="#">Forgot Password?</a></div>
    <button onclick="(u.value&&p.value)?alert('Bem-vindo, '+u.value+'!'):alert('Preencha todos os campos!')">LOGIN</button>
    <div class="links">Don't have an account? <a href="#">Sign up</a></div>
    <div class="social"><hr><p>Or</p>
      <button class="btn fb" disabled><img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Facebook_Logo_(2019).png">Login with Facebook</button>
      <button class="btn gg" disabled><img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAOEAAADhCAMAAAAJbSJIAAABfVBMVEX///8ZdtL/PQBMr1D/wQcAbs/Q3N6owun/MgD/vgD/vQD/NwD/LAD/MQD/wgD//vr/JABErUsoesEAbNH/RAD/bEH/xgc8qkE+q0X/7eT/9Ov/13Xo7u8Ab87/24X/+ev/49z/5tb/TgD/2sr/mXn/yLH/z7r/bjr/YC3/iFz/Zzn/4dL/YQL/7sb/9Nn/bQP/swb/xij/4JX/zEj/7805rlNZkcnN4rrW5sROnnmPxHqm0Zyey47m8eP/28X/wqb/pYX/k33/elr/YB//zsP/d1b/vKn/gFD/TBj/nYP/i2v/rpL/lXP/dEr/ZS7/YCT/hGz/fQD/oQb/z1f/kgX/6LP/3LujvMtwnslPjNLj6vOOsNF1odnZ4d//560xfcK6zt0WdcePsc/d1omTtTnuvxBsskfOvCNyu2mktzS1uS1jsUmyyuR2uFWQwW15rJBRp2HP3qw9ialKkpZRo205g7Wex3yMxodGlo08iKtMn3hTi7nB1prj57xisD7uzp0jAAAKU0lEQVR4nO2d+1/b1hXAhW0SgSTLCgYJB9cxBDeQkDVPu8bC5NFAeCVt+kiTZYEtbdg8WNJtpFspf/sky9iSLMnnXuneK3v6/tLHp8H3m3PuOUf3yinHJSQkJCQkJCQkJCQkJCQkJMCRDQrl62trlbW1crlg/iPrJUWFPHuluf7g4aN5QcwZiKL1l9T8o+cP1ptXZodbtPz46lfXUqIo8YIgpJwY/4aXRDG1/NXVx2XWC8Wi/GRjUxD5PjM3giCJwubGkwLrBSNRqDzI58SBcnZNMTf/tDIkGVtYfJgXebBcz5LP5bcq8Q/lwkZehMfODS9ubi2wVgiisD4fQq8TSXF+O67ZurAkSiH9LElR3LnOWsaDyjTO5vOBF3fjlqyVa2HT04UgTa+xlrJRmc9F69d2zO3FJVev7xLwsxyX4jDtFLYiKS/e8MJV5nV1OxVdffFCyi8y9Svv5Yj6pcxUnZ5lJ7hOMEFtjsITRn7lPZGCn4m4y2RcbRKqoF7wUoW6X2GJ+A50kKNdVMubElVBI1P3qBacJsLTbVQIKYpj3DrdDD1XzG1T8pOXaNVQN7mrdAQ/ZyVobMYlCoKFZ2THtGCkPeKdcXaefo2xGy6TNiznmQryy6S7YpltBPlrpAVnRz2CBcYRnCYtKD8b8QjKn7NsExT2IMdskrEEiacotz7qgotMhu2uIPkULY94keEKj0IbWpfaomje5EvS4LthuyD5FOWWQj3RC7yYSz17vrO+vVhZuLLweHF7fef5s1RO5EGaFCLINfE3oWl342lztu/lElmebT69AbCksAe5Mm4ZNRJzcyfwdl5e3NmUAiVppCi3jLcJBXFzB3ALKC9sBdwcUxHE64R8bncRurjC4rLP4SuNPciVcYY1XlxCu/y7vuEVR4mGILeHnqOCsIR+uFne6LsFoZKiGHVUEHfxLm8Xpp37QaIiWEAOoJTHv2NoCrYtQaNNGOwg9npB3AqzrsJSdztSKTJGAUAsM3yIAFos5q2PpLMHOW4XrcxEcdE32z5xphRBroJWZnLrUXyovJNLSXT2IMfd+hohhoIU1UsFzRylFOVWJme+AR8gCvnoXtRao3WrfSeTmZm8AaumQv4KpVVFyMpExmDmW8hjnJBn+E4INi8ybWa+GJypwyl4c8IyzGQn/zCgLQ5linLc5XPDwZkqxe1tUBClnqCZqUF3Fjm2757hcttumMlmvvbNVPEp67XicSvjZOYbnxNAfpf1UvG4O5FxK34x7xVGIR//70h4crnPMJOd8RriRPqvnEWC7E7STqb2tUZpi/VSMVnpD6GVqa4hTkgxf00ZE48k7WSqszUOaaMwkjTrLejOVGFI66j53ORr6Bji+KEcZkw+80nSThi/7Rxt8g9ZLxQbz0pqLzjWECfG4RsfWJQCktTK1PYQJ2ywXig23wUmqRVGY4jLxeWLSej49QpXpk6zXic+A7ZhJ1Mnvme9TmxKEMFM5tawjjO+I5uLic9wfvbcBQIgr+I2zPAmjuHFqfHIKb691OYH8CpegAxv4QhyF8fHSDH+EryKO+SSlKTh2I/QwlDK+s/dPSZXYmd4MAdcxE3YNsQSJGpYfAVcBKyU3omf4RS0qIJK6cTt+BmOQ4tp8KPTueF3MTR8DVzEZUiSTpbiZ1j8I3ARoGaRxRzZiBreBy4KNHdjFhqyhm9hhvIMQHDicgwNxy4BDUGFBm+iIWx4AFuDPOgIo22I2SzIGk7B1jDwkKZt+KdYGsLGNpgh3lQaD8ObEMPJu7E0fBOhIdbjb0wM74684ejHcPT34ejX0tHvh6M/0wzxXDoGNBzeZ4uDUX8+HAM+H/4fPOOP/jkN7KwNsyESNYSetQ3veemfgYsY2jPv8X3gImD3FpMxNITeW4z+3dPo3x8O6x1w8T54FXG7xy/CDMGlFPwuxl9wDHHexXjzG8gRXEqBpSb7Lk3rfRr5ABZEcKGBzN7Zn36+p1bJSTnYnwIJAs/02wx8ry37Pp1OK4fEnJzcByVpEf6yyeB3E7N/vWcYplWdmJSdN7AQjv8d4WcGH9WYGWoKppU6MSs7L2G1FHhI0yFoI7Yz1IJKEOeAHRRlGwZ2xOzf7nUNqQQRGELww6GF/7v6M+96gum0ViOk1eMCsN9P7SP9WL/vW2R/atkFaZRTWCEdQ+qGJt79Ivve4WfuRNI9EdgLUZPUb3B75xY0FMkONtBxBq1XtH9yfzXtNgkHhIvNS/CjCGKSeqSprUk4g0iy2OxDBRGenM5xf4e0M8Z4Qa4pzkFzFOW5oosjTb0zlHQ9lcF1FHpj4cDe9LPvW35+BlojcjeL1+BNCD4ptWP7Pr59jPHcimRaBrRRjKHOpOd0a03Wo0lQqDbQYWYMq86YdI5N3WOM916Mvtq8OgALYtUZkxdBTcJl2Ipace4AHsKxHzE/xJxrBmdoR1GLVhFJEHme6XInqEm4FSNti69QBMFXv/2sgDK0qxhdubmAJIgfQo47UhAUo2sa4FmtQ4iPqqkohml1NRLB1/A+aDIVIoQcd4wUxLR2iHn3bUP/B5ogdiHtfBxaECPYjLW0+iWSYJhdaNJAC6KRqY0wj8Ry3fgt1T4gFBrMcaZHKWjk9g5jiBGuqipWJryFz9zQe19fPiLmqRnGOl5rrB32PusX4GYEf9UpALSOYYVRw3DU65rtk7R/AhXDCyIXG8sRNY56XXX+TsLqDeIhqQ+nGoai4XhYg9YcuXqo9mWK9q/B9WYc9QjRB8Sm2HNsNSCB1Bvpfj/z13+4NKjewF++CKaEk6cdyXQjMJJyzUev/avT/w7ejNHkqAlGPe0tU1OPVqu6x/8bQa+u/qxqgfmh/hIURYTv3w/kBGsr2i3Pjj41Tk+rNV3Xa9WPq41PR2cD7CzFXwMUw41rTmSMltGnqSiapqkGmmb8PfBXBZXU0L3ejh4uiCHwHeHCzqNufg+xFcNh1BuvTJ26GK2g0RWZKabT/+lXHA87cHsQstqEQekb4YpRVpkumI0/CtQvnVEsRtXqnURRUHFxj3CRltEepRY7ReWD7ZEx/DNhLBV7JbW4T0qQrWJvhCMoyFrx1yLBPRgLRe2/xfEDwoKGIsOKaoxwvxFpE07kY3atXzsOf+IM4YTVAKeeUPHjmM2o6iktQY6rAR5eo0Zp/U5P0HhePKK9GbUjOluwi0x5M6on9P8o0arvGVn0KOpH6n4G+iGtTKXVJPo5pRJGhWYNdaMfkt+N6jHuH6MSDR8Jz6lKi8kOtFNqEExVRT1htQPt6MeEHBX1mM7XjgZTOyLgqKhH5L/MAafmcQE4Sn4mkToa+Rk3PxP9RI1mBNDUk7jsPzel1VboQCpq6zQO9dOXWt3/ThekdxLH9HRSqn06w5JU1LN6Ldbh6yHXVkE3vDY7TT1bBb+7EQ/0at2IyuC7XkUx/qvWcXVIgudCrzXqh632rbanm6aprcN6oxbXyglDLulV88WElqpad/jtq3z1rGW+ulDV9eHKzCBkA12vmRhaJqxXlJCQkJCQkJCQkJCQkJCQMFT8D+A9qt2p0niaAAAAAElFTkSuQmCC">Login with Google</button>
    </div>
  </div>
<script>
  eye.onclick=()=>{p.type=p.type==="password"?"text":"password";eye.textContent=p.type==="password"?"👁️":"";}
</script>
</body>
</html>
