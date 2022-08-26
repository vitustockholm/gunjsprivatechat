<script>
    import { username, user } from './user';
  
    function signout() {
      user.leave();
      username.set('');
    }
  </script>
  
  <header>
  <h1>🔫💬</h1>
    {#if $username}
      <div class="user-bio">
        
        <span>SVEIKI ATVYKĘ <strong>{$username}</strong></span>
        <img src={`https://avatars.dicebear.com/api/initials/${$username}.svg`} alt="avatar" /> 
      </div>
  
      <button class="signout-button" on:click={signout}>ATSIJUNGTI</button>
  
      {:else}
  
        <h3>CHIRC#</h3>
    {/if}
  </header>