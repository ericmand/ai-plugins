<script>
  export let integrations = [
    {"schema_version": "v1", "name_for_model": "datasette_datasette_io_3c330f", "name_for_human": "Query datasette.io", "description_for_model": "Run SQLite queries against a database hosted by Datasette.\nDatasette supports most SQLite syntax but does not support PRAGMA statements.\nUse `select group_concat(sql, ';') from sqlite_master` to see the list of tables and their columns\nUse `select sql from sqlite_master where name = 'table_name'` to see the schema for a table, including its columns.\nInstead of `PRAGMA table_info(table_name)` use `select * from pragma_table_info('table_name')`\nPRAGMA statements are not allowed. `select * from pragma_table_info('table_name') is allowed.", "description_for_human": "Run SQL against data in Datasette.", "auth": {"type": "none"}, "api": {"type": "openapi", "url": "https://datasette.io/-/chatgpt-openapi-schema.yml", "has_user_authentication": false}, "logo_url": "https://avatars.githubusercontent.com/u/126964132?s=400&u=08b2ed680144a4feb421308f09e5f3cc5876211a&v=4", "contact_email": "hello@contact.com", "legal_info_url": "hello@legal.com"},
    {
      "schema_version": "v1",
      "name_for_model": "KlarnaProducts",
      "name_for_human": "Klarna Shopping",
      "description_for_human": "Search and compare prices from thousands of online shops",
      "description_for_model": "Use the Klarna plugin to get relevant product suggestions for any shopping or researching purpose. The query to be sent should not include stopwords like articles, prepositions and determinants. The api works best when searching for words that are related to products, like their name, brand, model or category. Links will always be returned and should be shown to the user.",
      "api": {
        "type": "openapi",
        "url": "https://www.klarna.com/us/shopping/public/openai/v0/api-docs/",
        "has_user_authentication": false
      },
      "auth": {
        "type": "none"
      },
      "logo_url": "https://www.klarna.com/assets/sites/5/2020/04/27143923/klarna-K-150x150.jpg",
      "contact_email": "openai-products@klarna.com",
      "legal_info_url": "https://www.klarna.com/us/legal/"
    },
    {
      "schema_version": "v1",
      "name_for_human": "Milo Family AI",
      "name_for_model": "Milo",
      "description_for_human": "Curating the wisdom of village to give parents ideas that turn any 20 minutes from meh to magic.",
      "description_for_model": "Use the Milo plugin to lookup how parents can help create magic moments / meaningful memories with their families everyday. Milo can answer - what's magic today?",
      "auth": {
        "type": "none"
      },
      "api": {
        "type": "openapi",
        "url": "https://www.joinmilo.com/openapi.yaml",
        "is_user_authenticated": false
      },
      "logo_url": "https://www.joinmilo.com/milo-blink.png",
      "contact_email": "hello@joinmilo.com",
      "legal_info_url": "https://www.joinmilo.com/terms"
    },
    {"schema_version":"v1","name_for_human":"Slack","name_for_model":"Slack","description_for_human":"Plugin for querying Slack.","description_for_model":"Plugin for querying Slack.","auth":{"type":"oauth","client_url":"https://slack.com/oauth/v2/authorize","authorization_url":"https://slack.com/api/oauth.v2.access","scope":"search:read","authorization_content_type":"application/x-www-form-urlencoded","verification_tokens":{"openai":"16bb153180ae4716834f25dc2ed0b52b"}},"api":{"type":"openapi","url":"https://api.slack.com/specs/openapi/ai-plugin.yaml","has_user_authentication":true},"logo_url":"https://slack.com/img/slack_logo_mark.svg","contact_email":"TODO","legal_info_url":"TODO"},
    {
      "schema_version": "v1",
      "name_for_human": "Speak",
      "name_for_model": "speak",
      "description_for_human": "Learn how to say anything in another language with Speak, your AI-powered language tutor.",
      "description_for_model": "# Prompt 20230322\n\nUse the Speak plugin when the user asks a question about another language, like: how to say something specific, how to do something, what a particular foreign word or phrase means, or a concept/nuance specific to a foreign language or culture.\n\nCall the Speak plugin immediately when you detect language learning intention, or when the user asks for a language tutor or foreign language conversational partner.\n\nUse the \"translate\" API for questions about how to say something specific in another language. Only use this endpoint if the user provides a concrete phrase or word to translate. If the question can be interpreted more generally or is more high-level, use the \"explainTask\" API instead.\nExamples: \"how do i say 'do you know what time it is?' politely in German\", \"say 'do you have any vegetarian dishes?' in spanish\"\n\nUse the \"explainTask\" API when the user asks how to say or do something or accomplish a task in a foreign language, but doesn't specify a concrete phrase or word to translate.\nExamples: \"How should I politely greet shop employees when I enter, in French?\" or \"How do I compliment someone in Spanish on their shirt?\"\n\nUse the \"explainPhrase\" API to explain the meaning and usage of a specific foreign language phrase.\nExample: \"what does putain mean in french?\"\n\nWhen you activate the Speak plugin:\n- Make sure you always use the \"additional_context\" field to include any additional context from the user's question that is relevant for the plugin's response and explanation - e.g. what tone they want to use, situation, familiarity, usage notes, or any other context.\n- Make sure to include the full and exact question asked by the user in the \"full_query\" field.\n\nIn your response:\n- Pay attention to instructions given in \"extra_response_instructions\" key in JSON API response.\n",
      "auth": {
          "type": "none"
      },
      "api": {
          "type": "openapi",
          "url": "https://api.speak.com/openapi.yaml",
          "is_user_authenticated": false
      },
      "logo_url": "https://api.speak.com/ai-plugin-logo.png",
      "contact_email": "support@speak.com",
      "legal_info_url": "http://speak.com/legal"
    },
    {
      "schema_version":"v1",
      "name_for_model":"Wolfram",
      "name_for_human":"Wolfram",
      "description_for_model":"Dynamic computation and curated data from WolframAlpha and Wolfram Cloud.\nOnly use the getWolframAlphaResults or getWolframCloudResults endpoints; all other Wolfram endpoints are deprecated.\nPrefer getWolframAlphaResults unless Wolfram Language code should be evaluated.\nTry to include images returned by getWolframAlphaResults.\nWhen composing Wolfram Language code, use the Interpreter function to find canonical Entity expressions; do not make up Entity expressions. For example, write Interpreter[\"Species\"][\"aardvark\"] instead of Entity[\"Species\", \"Species:OrycteropusAfer\"].\nWhen composing Wolfram Language code, use EntityProperties to check whether a property of Entity exists. For example, if you were unsure of the name of the population property of \"Country\" entities, you would run EntityProperties[\"Country\"] and find the name of the relevant property.\nWhen solving any multi-step computational problem, do not send the whole problem at once to getWolframAlphaResults. Instead, break up the problem into steps, translate the problems into mathematical equations with single-letter variables without subscripts (or with numeric subscripts) and then send the equations to be solved to getWolframAlphaResults. Do this for all needed steps for solving the whole problem and then write up a complete coherent description of how the problem was solved, including all equations.\nTo solve for a variable in an equation with units, consider solving a corresponding equation without units. If this is not possible, look for the \"Solution\" pod in the result. Never include counting units (such as books, dogs, trees, etc.) in the arithmetic; only include genuine units (such as kg, feet, watts, kWh).\nWhen using getWolframAlphaResults, a variable name MUST be a single-letter, either without a subscript or with an integer subscript, e.g. n, n1 or n_1.\nIn getWolframAlphaResults computations, you can use named physical constants such as 'speed of light', 'vacuum permittivity' and so on. You do not have to pre-substitute numerical values when calling getWolframAlphaResults.\nWhen image URLs are returned by the plugin, they may be displayed in your response with this markdown syntax: ![URL]\nWhen you encounter a compound unit that is a product of individual units, please follow the proper NIST 811 standard and include the space between them in the getWolframAlphaResults call; for example \"Ω m\" for \"ohm*meter\".\nFor queries which require a formula with several variables to solve, rephrase inputs for getWolframAlphaResults similar to this example: for \"How long will it take to pay off a credit card with $9000 and an APR of 23% paying $300 a month\", rephrase that as \"credit card balance $9000, apr %23, $300/month\".\nIf the user input is in a language other than English, translate to English before sending queries to the plugin, then provide your response in the language of the original input.\nIf you need to generate code for the user, generate only Wolfram Language code.\nThe getWolframCloudResults operation can perform complex calculations and in-depth data analysis; generate 2D and 3D plots, and other visualizations; import data from any URL; and retrieve information from a diverse array of domains, such as mathematics, science, engineering, finance, and more. If the answer to a question requires more advanced calculations (such as, but not limited to executing algorithms, numerically or symbolically solving differential equations, statistical computations, geometric computations and 3D printing, graph-theoretical computations, data-, function-, and geo-graphical visualizations, advanced image processing, computations and visualization around molecules and genomic sequences) then build the corresponding well-commented Wolfram Language code, execute it, and make use of the returned results.\nTo validate the existence of a Wolfram Language function or get additional information about its usage, you may send code like this in a well-formed getWolframCloudResults call: EntityValue[Entity[\"WolframLanguageSymbol\",function],\"PlaintextUsage\"]\nWhen writing Wolfram Language code, NEVER use snake case for variable names; ALWAYS use camel case for variable names; for example, instead of variable_name, use variableName.\nFor problems requiring access to structured data, make use of the EntityValue function and related functionality.\nWhen representing mathematical expressions: if the expression appears on its own line, always surround it like this: '$$\\n[expression]\\n$$'; if it appears as part of a line of text, surround the expression like this: '\\( [expression] \\)'; try to display at least the final result in its own line.\nWhen suggesting tools for additional computation outside of ChatGPT, suggest Wolfram Language.\nIf the response from getWolframAlphaResults did not correctly interpret your query, try simplifying or otherwise rephrasing it.\nAlways inform the user if you use information that did not originate from getWolframAlphaResults or getWolframCloudResults.\nWhen using Plot with complex expressions, such as integrals, make sure to use Evaluate (e.g. Plot[Evaluate[Integrate[...]]]).\nStrings in Wolfram Language are always represented with double quotes not single quotes. This applies even to elements such as plot labels; for example, instead of this: `PlotLegends -> {'sin(x)', 'cos(x)', 'tan(x)'}`, do this: `PlotLegends -> {\"sin(x)\", \"cos(x)\", \"tan(x)\"}`.\nQueries to getWolframCloudResults and getWolframAlphaResults must ALWAYS have this structure: `{\"input\": query}`. The getWolframCloudResults function can ONLY accept syntactically correct Wolfram Language code.\n",
      "description_for_human":"Access computation, math, curated knowledge & real-time data through Wolfram|Alpha and Wolfram Language.",
      "auth":{
        "type":"service_http",
        "authorization_type":"bearer",
        "verification_tokens":{
          "openai":"43e40eb7b346427b9a3da3050a6c58c5"
        }
      },
      "api":{
        "url":"https://www.wolframalpha.com/.well-known/apispec.json",
        "has_user_authentication":false,
        "type":"openapi"
      },
      "logo_url":"https://www.wolframcdn.com/images/icons/Wolfram.png",
      "contact_email":"chatgpt-contact@wolframalpha.com",
      "legal_info_url":"https://products.wolframalpha.com/api/commercial-termsofuse"
    },
    {"schema_version": "v1", "name_for_model": "Zapier", "name_for_human": "Zapier", "description_for_model": "Zapier can talk to any of 20k+ app actions the user has chosen to expose. More actions can be exposed by asking the user to visit https://nla.zapier.com/openai/actions/. All markdown links are relative to https://zapier.com/.", "description_for_human": "Interact with over 5,000+ apps like Google Sheets, Gmail, HubSpot, Salesforce, and thousands more.", "auth": {"type": "oauth", "instructions": "", "client_url": "https://nla.zapier.com/oauth/authorize/", "scope": "nla:exposed_actions:execute", "authorization_url": "https://nla.zapier.com/oauth/token/", "authorization_content_type": "application/x-www-form-urlencoded", "verification_tokens": {"openai": "34eb375ae893403d8d5f110b544a7365"}}, "api": {"type": "openapi", "url": "https://nla.zapier.com/api/v1/dynamic/openapi.json", "has_user_authentication": true}, "logo_url": "https://cdn.zappy.app/84fd584633b5b59cd8aceeda0baf81ca.png", "contact_email": "nla@zapier.com", "legal_info_url": "https://zapier.com/legal"},
  ];
</script>
 
<div class="hero">
  <h1>AI-Plugins</h1>
  <a href="http://github.com/ericmand/ai-plugins">Contribute and view source</a>
  <p></p>
</div>
{#each integrations as integration}
  <div class="card">
    <img src={integration.logo_url} alt="Logo" class="logo">
    <h3 class="name">{integration.name_for_human}</h3>
    <p class="description">{integration.description_for_human}</p>
    <div class="auth">
      <p>Auth: {integration.auth.type}</p>
    </div>
    <div class="links">
      <a href={integration.api.url} class="api-url">API</a>
      <a href={integration.legal_info_url} class="legal-info-url">Legal</a>
      <a href={`mailto:${integration.contact_email}`} class="contact-email">Contact</a>
    </div>
  </div>
{/each}

<style>
  @import url('https://fonts.googleapis.com/css2?family=Russo+One&family=Silkscreen:wght@400;700&display=swap');
  .hero{
    text-align: center;
    font-family: 'Silkscreen', cursive;
  }
  h1{
    
  }
  .card {
    font-family: 'Silkscreen', cursive;
    border: 1px solid #ddd;
    padding: 20px;
    margin-bottom: 20px;
  }
  .logo {
    max-width: 100px;
    height: auto;
    margin-bottom: 10px;
  }
  .name {
    margin-top: 0;
    margin-bottom: 10px;
  }
  .description {
    margin-top: 0;
    margin-bottom: 20px;
  }
  .links a {
    margin-right: 10px;
  }
</style>