<script>
    let firstName = '';
    let lastName = '';
    let email = '';
    let password = '';
  
    function handleSubmit(event) {
      event.preventDefault();
      console.log(`Submitted: ${firstName} ${lastName} (${email}) - ${password}`);
      // You can add your login logic here
    }
  </script>
  
  <form on:submit={handleSubmit} class='flex flex-col border-2 w-1/4 bg-slate-300 gap-1 p-2 items-center'>
    <label>
      First Name:
      <input type="text" bind:value={firstName} required>
    </label>
    <label>
      Last Name:
      <input type="text" bind:value={lastName} required>
    </label>
    <label>
      Email:
      <input type="email" bind:value={email} required>
    </label>
    <label>
      Password:
      <input type="password" bind:value={password} required>
    </label>
    <button type="submit">Login</button>
  </form>
  