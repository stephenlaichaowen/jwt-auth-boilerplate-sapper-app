<script>
	export let segment;
</script>

<style>
	nav {
		border-bottom: 1px solid rgba(255,62,0,0.1);
		font-weight: 300;
		padding: 0 1em;
	}

	ul {
		margin: 0;
		padding: 0;
    display: flex;
	}

	/* clearfix */
	ul::after {
		content: '';
		display: block;
		clear: both;
	}

	li {
		display: block;
		float: left;
  }
  
  .logout {
    margin-left: auto;
  }

	[aria-current] {
		position: relative;
		display: inline-block;
	}

	[aria-current]::after {
		position: absolute;
		content: '';
		width: calc(100% - 1em);
		height: 2px;
		background-color: rgb(255,62,0);
		display: block;
		bottom: -1px;
	}

	a {
		text-decoration: none;
		padding: 1em 0.5em;
		display: block;
	}
</style>

<nav>
	<ul>
		<li><a aria-current='{segment === undefined ? "page" : undefined}' href='.'>home</a></li>	
		<li><a aria-current='{segment === "profile" ? "page" : undefined}' href='profile'>profile</a></li>
		<li><a aria-current='{segment === "organization" ? "page" : undefined}' href='organization'>my organization</a></li>
		<li><a aria-current='{segment === "admin" ? "page" : undefined}' href='admin'>admin tools</a></li>		
		<li class="logout"><a aria-current='{segment === "logout" ? "page" : undefined}' href='logout'>log out</a></li>
	</ul>
</nav>
