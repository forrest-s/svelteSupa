<script>
    let firstName = '';
    let lastName = '';
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
  
  <form on:submit={handleSubmit} class='flex flex-col border-2 rounded w-1/3 gap-2 p-2 items-center'>
    <label class={labelClass}>
      First Name
      <input class={inputClass} type="text" bind:value={firstName} required>
    </label>
    <label class={labelClass}>
      Last Name
      <input class={inputClass} type="text" bind:value={lastName} required>
    </label>
    <label class={labelClass} >
      Email
      <input class={inputClass} type="email" bind:value={email} required>
    </label>
    <label class={labelClass} >
      Password
      <input class={inputClass} type="password" bind:value={password} required>
    </label>
    <button class='btn btn-sm btn-secondary' type="submit">Register</button>
  </form>
  