<script>
  const helloArr = [
    'hello',
    'bonjour',
    'holla',
    '你好',
    'hallo',
    'Здравствуйте',
    'ciao',
    'नमस्कार',
    'olà',
    'مرحبا'
  ]

    let hello = "hello!"
  //hello loop
  let i = 0;
  let intervalId = setInterval(() => {
      hello = helloArr[i] + "!";
      if (i === helloArr.length) {
          i = 0;
          clearInterval(intervalId);
          hello = helloArr[0] + "!";
      } else {
          i++;
      }
  }, 1500);
</script>

<div>
    <h1 id="hello">{ hello }</h1>
</div>