<script>
    let email = '';
    let password = '';
  
    let labelClass = 'flex flex-col'
    let inputClass = 'rounded'
    
    function handleSubmit(event) {
      event.preventDefault();
      console.log(`Submitted: ${firstName} ${lastName} (${email}) - ${password}`);
      // You can add your login logic here
    }
  </script>
  
  <form on:submit={handleSubmit} class='flex flex-col border-2 w-1/4 bg-slate-300 gap-1 p-2 items-center'>
    <label class={labelClass}>
      Email:
      <input class={inputClass} type="email" bind:value={email} required>
    </label>
    <label class={labelClass}>
      Password:
      <input class={inputClass} type="password" bind:value={password} required>
    </label>
    <button type="submit">Login</button>
  </form>
  