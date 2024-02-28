<html>
<body>



<script>
  const scriptURL = 'https://script.google.com/macros/s/AKfycbxytVEv5K-gtAU-zMC9cBdzQDMzm9FszxGjsG4CU_FIyphcBeOeQeDPS77zp4ZTo1S8mQ/exec'
  const form = document.forms['submit-to-google-sheet']

  form.addEventListener('submit', e => {
    e.preventDefault()
    fetch(scriptURL, { method: 'POST', body: new FormData(form)})
      .then(response => console.log('Success!', response))
      .catch(error => console.error('Error!', error.message))
  })
</script>

</body>
</html>

