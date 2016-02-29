<h2> Unofficial Google Play Store API <strong> <a href='http://thetutlage.com/post=TUT269' title='Documentation'>@aman virk </a> </strong></h2>


### Introduction ###
<p>Play Store API is an unofficial version of <strong>Google Play Store</strong> which will let you pullup applications from google play store using<br>
18 different functions covering almost everything from google store<br>
</p>

### Requirements ###
<ol>
<blockquote><li> Php 5.0 or greater</li>
<li> <a href='http://php.net/manual/en/book.curl.php' title='CURL'> CURL </a> enabled server </li>
<li> Support for <a href='http://php.net/manual/en/function.mb-eregi.php' title='mb_eregi'> mb_eregi </a> function. </li>
</ol></blockquote>

### Error Handling ###
<p> Class itself does all required error handling. All functions will return <strong>0</strong> in case of any error and will return array of data in case of success.</p>

### List Of Functions ###
<ol>
<blockquote><li><a href='#topPaidApps' title='Top Paid Apps'> Getting Top Paid Apps </a></li>
<li><a href='#topFreeApps' title='Top Free Apps'> Getting Top Free Apps</a></li>
<li><a href='#topGrossingApps' title='Top Grossing Apps'> Getting Top Grossing Apps</a></li>
<li><a href='#topNewPaidApps' title='Top New Paid Apps'> Getting Top New Paid Apps</a></li>
<li><a href='#topNewFreeApps' title='Top Free Apps'> Getting Top New Free Apps</a></li>
<li><a href='#topPaidGames' title='Top Paid Games'> Getting Top Paid Games</a></li>
<li><a href='#topFreeGames' title='Top Free Games'> Getting Top Free Games</a></li>
<li><a href='#topTrendingApps' title='Getting Trending Apps'> Getting Trending Apps </a></li>
<li><a href='#staffPicks' title='Getting Staff Picks'> Getting Staff Picks </a></li>
<li><a href='#staffPicksForTablet' title='Getting Staff Picks For Tablet'> Getting Staff Picks For Tablet </a></li>
<li><a href='#listCategories' title='List Categories'> List All Categories</a></li>
<li><a href='#categoryPaidItems' title='Finding Paid Category Items'> Finding Paid Items In A Category </a></li>
<li><a href='#categoryFreeItems' title='Finding Free Items In A Category'> Finding Free Items In A Category </a></li>
<li><a href='#developerItems' title='Finding Items From A Certain Developer'> Finding Items From A Certain Developer </a></li>
<li><a href='#searchStore' title='Search Items'> Search Items </a></li>
<li><a href='#itemInfo' title='Getting Item Info'> Getting Item Info </a></li>
<li><a href='#relatedViewed' title='Finding Related Viewed Items'> Finding Related Viewed Items </a></li>
<li><a href='#relatedInstalled' title='Finding Related Installed'> Finding Related Installed </a></li>
</ol></blockquote>

<div>
<blockquote><h3>Getting Top Paid Apps</h3></blockquote>

<pre><code>		include_once('api/playStoreApi.php'); // including class file<br>
		$class_init = new PlayStoreApi;	// initiating class<br>
<br>
		/* WITHOUT PARAMERTER */<br>
		$topPaidApps = $class_init-&gt;topPaidApps(); // calling topPaidApps<br>
<br>
		/* PAGINATION PARAMETER */<br>
		// You can easily add the page numbers to paginate the result<br>
		$page = 2;<br>
		$topPaidApps = $class_init-&gt;topPaidApps($page); // calling topPaidApps<br>
<br>
		if($topPaidApps !== 0)<br>
		{<br>
			print_r($topPaidApps); // it will show all data inside an array<br>
		}<br>
</code></pre>
</div>

<div>
<blockquote><h3>Getting Top Free Apps</h3>
<pre><code>		include_once('api/playStoreApi.php'); // including class file<br>
		$class_init = new PlayStoreApi;	// initiating class<br>
<br>
		/* WITHOUT PARAMERTER */<br>
		$topFreeApps = $class_init-&gt;topFreeApps(); // calling topFreeApps<br>
<br>
		/* PAGINATION PARAMETER */<br>
		// You can easily add the page numbers to paginate the result<br>
		$page = 2;<br>
		$topFreeApps = $class_init-&gt;topFreeApps($page); // calling topFreeApps<br>
<br>
		if($topFreeApps !== 0)<br>
		{<br>
			print_r($topFreeApps); // it will show all data inside an array<br>
		}<br>
</code></pre>
</div></blockquote>

<div>
<blockquote><h3>Getting Top Grossing Apps</h3>
<pre><code>		include_once('api/playStoreApi.php'); // including class file<br>
		$class_init = new PlayStoreApi;	// initiating class<br>
<br>
		/* WITHOUT PARAMERTER */<br>
		$topGrossingApps = $class_init-&gt;topGrossingApps(); // calling topGrossingApps<br>
<br>
		/* PAGINATION PARAMETER */<br>
		// You can easily add the page numbers to paginate the result<br>
		$page = 2;<br>
		$topGrossingApps = $class_init-&gt;topGrossingApps($page); // calling topGrossingApps<br>
<br>
		if($topGrossingApps !== 0)<br>
		{<br>
			print_r($topGrossingApps); // it will show all data inside an array<br>
		}<br>
</code></pre>
</div></blockquote>

<div>
<blockquote><h3>Getting Top New Paid Apps</h3>
<pre><code>		include_once('api/playStoreApi.php'); // including class file<br>
		$class_init = new PlayStoreApi;	// initiating class<br>
<br>
		/* WITHOUT PARAMERTER */<br>
		$topNewPaidApps = $class_init-&gt;topNewPaidApps(); // calling topNewPaidApps<br>
<br>
		/* PAGINATION PARAMETER */<br>
		// You can easily add the page numbers to paginate the result<br>
		$page = 2;<br>
		$topNewPaidApps = $class_init-&gt;topNewPaidApps($page); // calling topNewPaidApps<br>
<br>
		if($topNewPaidApps !== 0)<br>
		{<br>
			print_r($topNewPaidApps); // it will show all data inside an array<br>
		}<br>
</code></pre>
</div></blockquote>

<div>
<blockquote><h3>Getting Top New Free Apps</h3>
<pre><code>		include_once('api/playStoreApi.php'); // including class file<br>
		$class_init = new PlayStoreApi;	// initiating class<br>
<br>
		/* WITHOUT PARAMERTER */<br>
		$topNewFreeApps = $class_init-&gt;topNewFreeApps(); // calling topNewFreeApps<br>
<br>
		/* PAGINATION PARAMETER */<br>
		// You can easily add the page numbers to paginate the result<br>
		$page = 2;<br>
		$topNewFreeApps = $class_init-&gt;topNewFreeApps($page); // calling topNewFreeApps<br>
<br>
		if($topNewFreeApps !== 0)<br>
		{<br>
			print_r($topNewFreeApps); // it will show all data inside an array<br>
		}<br>
</code></pre>
</div></blockquote>

<div>
<blockquote><h3>Getting Top Paid Games</h3>
<pre><code>		include_once('api/playStoreApi.php'); // including class file<br>
		$class_init = new PlayStoreApi;	// initiating class<br>
<br>
		/* WITHOUT PARAMERTER */<br>
		$topPaidGames = $class_init-&gt;topPaidGames(); // calling topPaidGames<br>
<br>
		/* PAGINATION PARAMETER */<br>
		// You can easily add the page numbers to paginate the result<br>
		$page = 2;<br>
		$topPaidGames = $class_init-&gt;topPaidGames($page); // calling topPaidGames<br>
<br>
		if($topPaidGames !== 0)<br>
		{<br>
			print_r($topPaidGames); // it will show all data inside an array<br>
		}<br>
</code></pre>
</div></blockquote>

<div>
<blockquote><h3>Getting Top Free Games</h3>
<pre><code>		include_once('api/playStoreApi.php'); // including class file<br>
		$class_init = new PlayStoreApi;	// initiating class<br>
<br>
		/* WITHOUT PARAMERTER */<br>
		$topFreeGames = $class_init-&gt;topFreeGames(); // calling topFreeGames<br>
<br>
		/* PAGINATION PARAMETER */<br>
		// You can easily add the page numbers to paginate the result<br>
		$page = 2;<br>
		$topFreeGames = $class_init-&gt;topFreeGames($page); // calling topFreeGames<br>
<br>
		if($topFreeGames !== 0)<br>
		{<br>
			print_r($topFreeGames); // it will show all data inside an array<br>
		}<br>
</code></pre>
</div></blockquote>

<div>
<blockquote><h3>Getting Trending Apps</h3>
<pre><code>		include_once('api/playStoreApi.php'); // including class file<br>
		$class_init = new PlayStoreApi;	// initiating class<br>
<br>
		/* WITHOUT PARAMERTER */<br>
		$topTrendingApps = $class_init-&gt;topTrendingApps(); // calling topTrendingApps<br>
<br>
		/* PAGINATION PARAMETER */<br>
		// You can easily add the page numbers to paginate the result<br>
		$page = 2;<br>
		$topTrendingApps = $class_init-&gt;topTrendingApps($page); // calling topTrendingApps<br>
<br>
		if($topTrendingApps !== 0)<br>
		{<br>
			print_r($topTrendingApps); // it will show all data inside an array<br>
		}<br>
</code></pre>
</div></blockquote>

<div>
<blockquote><h3>Getting Staff Picks</h3>
<pre><code>		include_once('api/playStoreApi.php'); // including class file<br>
		$class_init = new PlayStoreApi;	// initiating class<br>
<br>
		/* WITHOUT PARAMERTER */<br>
		$staffPicks = $class_init-&gt;staffPicks(); // calling staffPicks<br>
<br>
		/* PAGINATION PARAMETER */<br>
		// You can easily add the page numbers to paginate the result<br>
		$page = 2;<br>
		$staffPicks = $class_init-&gt;staffPicks($page); // calling staffPicks<br>
<br>
		if($staffPicks !== 0)<br>
		{<br>
			print_r($staffPicks); // it will show all data inside an array<br>
		}<br>
</code></pre>
</div></blockquote>

<div>
<blockquote><h3>Getting Staff Picks For Tablet</h3>
<pre><code>		include_once('api/playStoreApi.php'); // including class file<br>
		$class_init = new PlayStoreApi;	// initiating class<br>
<br>
		/* WITHOUT PARAMERTER */<br>
		$staffPicksForTablet = $class_init-&gt;staffPicksForTablet(); // calling staffPicksForTablet<br>
<br>
		/* PAGINATION PARAMETER */<br>
		// You can easily add the page numbers to paginate the result<br>
		$page = 2;<br>
		$staffPicksForTablet = $class_init-&gt;staffPicksForTablet($page); // calling staffPicksForTablet<br>
<br>
		if($staffPicksForTablet !== 0)<br>
		{<br>
			print_r($staffPicksForTablet); // it will show all data inside an array<br>
		}<br>
</code></pre>
</div></blockquote>

<div>
<blockquote><h3>List All Categories</h3>
<pre><code>		include_once('api/playStoreApi.php'); // including class file<br>
		$class_init = new PlayStoreApi;	// initiating class<br>
<br>
		$listCategories = $class_init-&gt;listCategories(); // calling listCategories<br>
<br>
		if($listCategories !== 0)<br>
		{<br>
			print_r($listCategories['Games']); // it will show all games cateogry inside an array<br>
			print_r($listCategories['Applications']); // it will show all games cateogry inside an array<br>
		}<br>
</code></pre>
</div></blockquote>

<div>
<blockquote><h3>Finding Paid Items In A Category</h3>
<pre><code>		include_once('api/playStoreApi.php'); // including class file<br>
		$class_init = new PlayStoreApi;	// initiating class<br>
<br>
		/* WITHOUT PAGINATION PARAMERTER */<br>
		$category_name = 'Themes'<br>
		$categoryPaidItems = $class_init-&gt;categoryPaidItems($category_name); // calling categoryPaidItems<br>
<br>
		/* PAGINATION PARAMETER */<br>
		// You can easily add the page numbers to paginate the result<br>
		$page = 2;<br>
		$categoryPaidItems = $class_init-&gt;categoryPaidItems($category_name,$page); // calling categoryPaidItems<br>
<br>
		if($categoryPaidItems !== 0)<br>
		{<br>
			print_r($categoryPaidItems); // it will show all data inside an array<br>
		}<br>
</code></pre>
</div></blockquote>

<div>
<blockquote><h3>Getting Free Items In A Category</h3>
<pre><code>		include_once('api/playStoreApi.php'); // including class file<br>
		$class_init = new PlayStoreApi;	// initiating class<br>
<br>
		/* WITHOUT PAGINATION PARAMERTER */<br>
		$category_name = 'Themes'<br>
		$categoryFreeItems = $class_init-&gt;categoryFreeItems($category_name); // calling categoryFreeItems<br>
<br>
		/* PAGINATION PARAMETER */<br>
		// You can easily add the page numbers to paginate the result<br>
		$page = 2;<br>
		$categoryFreeItems = $class_init-&gt;categoryFreeItems($category_name,$page); // calling categoryFreeItems<br>
<br>
		if($categoryFreeItems !== 0)<br>
		{<br>
			print_r($categoryFreeItems); // it will show all data inside an array<br>
		}<br>
</code></pre>
</div></blockquote>

<div>
<blockquote><h3>Finding Items From A Certain Developer</h3>
<pre><code>		include_once('api/playStoreApi.php'); // including class file<br>
		$class_init = new PlayStoreApi;	// initiating class<br>
<br>
		/* WITHOUT PAGINATION PARAMERTER */<br>
		$developer_name = 'ZYNGA'<br>
		$developerItems = $class_init-&gt;developerItems($developer_name); // calling developerItems<br>
<br>
		/* PAGINATION PARAMETER */<br>
		// You can easily add the page numbers to paginate the result<br>
		$page = 2;<br>
		$developerItems = $class_init-&gt;developerItems($developer_name,$page); // calling developerItems<br>
<br>
		if($developerItems !== 0)<br>
		{<br>
			print_r($developerItems); // it will show all data inside an array<br>
		}<br>
</code></pre>
</div></blockquote>

<div>
<blockquote><h3>Search Items</h3>
<pre><code>		include_once('api/playStoreApi.php'); // including class file<br>
		$class_init = new PlayStoreApi;	// initiating class<br>
<br>
		/* SEARCH PARAMETERE */<br>
		$search_query = 'Go Themes';<br>
		$sort = 'Popularity'	// Popularity OR Relevance ( OPTIONAL )<br>
		$price = 'All'	// Free OR Paid OR All ( OPTIONAL )<br>
		$safe_search = 'Off' 	// Off OR On	( OPTIONAL )<br>
<br>
		/* WITHOUT PAGINATION PARAMERTER */<br>
<br>
		$searchStore = $class_init-&gt;searchStore($search_query,$sort,$price,$safe_search); // calling searchStore<br>
<br>
		/* PAGINATION PARAMETER */<br>
		// You can easily add the page numbers to paginate the result<br>
		$page = 2;<br>
		$searchStore = $class_init-&gt;searchStore($search_query,$sort,$price,$safe_search,$page); // calling searchStore<br>
<br>
		if($searchStore !== 0)<br>
		{<br>
			print_r($searchStore); // it will show all data inside an array<br>
		}<br>
</code></pre>
</div></blockquote>

<div>
<blockquote><h3>Getting Item Info</h3>
<pre><code>		include_once('api/playStoreApi.php'); // including class file<br>
		$class_init = new PlayStoreApi;	// initiating class<br>
<br>
		/* WITHOUT PAGINATION PARAMERTER */<br>
		$item_id = 'com.golauncher.go'<br>
		$itemInfo = $class_init-&gt;itemInfo($item_id); // calling itemInfo<br>
<br>
		if($itemInfo !== 0)<br>
		{<br>
			print_r($itemInfo); // it will show all data inside an array<br>
		}<br>
</code></pre>
</div></blockquote>

<div>
<blockquote><h3>Finding Related Viewed Items</h3>
<pre><code>		include_once('api/playStoreApi.php'); // including class file<br>
		$class_init = new PlayStoreApi;	// initiating class<br>
<br>
		/* WITHOUT PAGINATION PARAMERTER */<br>
		$item_id = 'com.golauncher.go'<br>
		$relatedViewed = $class_init-&gt;relatedViewed($item_id); // calling relatedViewed<br>
<br>
		if($relatedViewed !== 0)<br>
		{<br>
			print_r($relatedViewed); // it will show all data inside an array<br>
		}<br>
</code></pre>
</div></blockquote>

<div>
<blockquote><h3>Finding Related Installed</h3>
<pre><code>		include_once('api/playStoreApi.php'); // including class file<br>
		$class_init = new PlayStoreApi;	// initiating class<br>
<br>
		/* WITHOUT PAGINATION PARAMERTER */<br>
		$item_id = 'com.golauncher.go'<br>
		$relatedInstalled = $class_init-&gt;relatedInstalled($item_id); // calling relatedInstalled<br>
<br>
		if($relatedInstalled !== 0)<br>
		{<br>
			print_r($relatedInstalled); // it will show all data inside an array<br>
		}<br>
</code></pre>
</div>