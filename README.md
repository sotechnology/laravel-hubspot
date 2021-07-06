<h2>This will create contact in hubspot and get all contacts from hubspot for Laravel 5</h2>

Forked from nirbhay94/laravel-hubspot to support Laravel 5.1

<h3>Installation</h3>

1.<code>composer require nirbhay94/laravel-hubspot:dev-master</code>

2.Get a HubSpot API Key from the Intergrations page of your HubSpot account.

3.Add your HubSpot API key into the your <code>.env</code> file: <code>HAPI_KEY=yourApiKey</code>

4.Add <code>Nirbhay\Hubspot\HubspotServiceProvider::class</code> to your providers in your config/app.php file.

5.Add <code>'HubSpot' => Nirbhay\Hubspot\Facades\Hubspot::class</code> to your aliases in your config/app.php file.

6.<code>php artisan vendor:publish --provider="Nirbhay\Hubspot\HubspotServiceProvider"</code> will create a config/hubspot.php file.

<h3>Usage</h3>

You can use the facade as a dependency:

<h3>Facade</h3>

<pre><span class="pl-s1"><span class="pl-c"><span class="pl-c">//</span>Echo all contacts </span></span>
<span class="pl-s1"><span class="pl-smi">$response</span> <span class="pl-k">=</span> <span class="pl-c1">HubSpot</span><span class="pl-k">::</span>contacts()<span class="pl-k">;</span>
</pre>

<pre><span class="pl-s1"><span class="pl-c"><span class="pl-c">//</span>Create a contact </span></span>
<span class="pl-s1"><span class="pl-smi">$response</span> <span class="pl-k">=</span> <span class="pl-c1">HubSpot</span><span class="pl-k">::</span>createContact($request->only(['firstname', 'lastname', 'email','phone','website','company','address','city','state','zip']))<span class="pl-k">;</span>
</pre>
