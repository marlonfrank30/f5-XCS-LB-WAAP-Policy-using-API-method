
<p>This guide provides instructions on how to generate various credentials related to F5® Distributed Cloud Services from the platform.</p>
<p>F5® Distributed Cloud Console provides two types of credentials:</p>
<ul>
<li>
<p><code>My credentials</code>: Are generated and used for different authentication and authorization purposes while accessing F5® Distributed Cloud Services APIs or deploying apps using F5® Distributed Cloud Services vK8s.</p>
</li>
<li>
<p><code>Service credentials</code>: Are generated by administrators to create custom service roles that are associated with service users.</p>
</li>
</ul>
<blockquote>
<p><strong>Note</strong>: The <code>My Credentials</code> inherit the roles of the users. In case of service credentials, you can assign specific roles to the service user.</p>
</blockquote>
<p>Using the instructions provided in this guide, you can create various types of credentials and download them for using in API requests.</p>
<hr>
<h2 id="prerequisites">Prerequisites</h2>
<p>The following prerequisites apply:</p>
<ul>
<li>A valid <a href="https://console.ves.volterra.io">Account</a> is required.</li>
</ul>
<blockquote>
<ul>
<li>Note: If you do not have an account, visit <a href="/docs/quick-start/on-board">Create an Account</a>.</li>
</ul>
</blockquote>
<ul>
<li>A single-node or multi-node F5® Distributed Cloud Services site in case of application deployment.</li>
</ul>
<blockquote>
<ul>
<li>Note: If you do not have a site, visit <a href="/docs/how-to/site-management">Site Management</a>.</li>
</ul>
</blockquote>
<hr>
<h2 id="my-credentials">My Credentials</h2>
<p><code>My Credentials</code> options can be generated and downloaded from the Console:</p>
<ul>
<li>
<p>API Tokens: The tokens are used in site deployment, and also for the authorization in the API requests.</p>
</li>
<li>
<p>X.509 Certificates: These certificates are used in API requests.</p>
</li>
<li>
<p>vK8s KubeConfig: These are the vK8s KubeConfigs for deploying your applications using F5® Distributed Cloud Services vK8s.</p>
</li>
</ul>
<blockquote>
<p><strong>Note</strong>: You can use either API certificate or API token for authenticating. It is recommended to use API certificates as they offer more robust security via Mutual TLS (mTLS) authentication. The API tokens are used with one-way TLS authentication.</p>
</blockquote>
<h3 id="generate-api-certificate">Generate API Certificate</h3>
<p>Features can be viewed, and managed in multiple services.</p>
<p>This example shows <code>Credentials</code> setup in <code>Administration</code>.</p>
<details>
<summary><b>Step 1:</b> Open <CODE>F5® Distributed Cloud Console</CODE> > select <CODE>Create Credentials</CODE>.</summary>  
<ul>
<li>Open <code>F5® Distributed Cloud Console</code> homepage, select <code>Administration</code> box.</li>
</ul>
<p><figure class="gatsby-resp-image-figure" style="">
    <span
      class="gatsby-resp-image-wrapper"
      style="position: relative; display: block; margin-left: auto; margin-right: auto; max-width: 2000px; "
    >
      <span
    class="gatsby-resp-image-background-image"
    style="padding-bottom: 53.2%; position: relative; bottom: 0; left: 0; background-image: url('data:image/webp;base64,UklGRjgAAABXRUJQVlA4ICwAAADQAgCdASoUAAsAPtFUo0uoJKMhsAgBABoJaQAAe/QAAP7xh2uypzsBWHkAAA=='); background-size: cover; display: block;"
  ></span>
  <picture>
          <source
              srcset="/docs/static/6cc23f597999ee52e128305c6621bd91/10636/NEW_HOME_PAGE_C.webp 500w,
/docs/static/6cc23f597999ee52e128305c6621bd91/e00f7/NEW_HOME_PAGE_C.webp 1000w,
/docs/static/6cc23f597999ee52e128305c6621bd91/56b60/NEW_HOME_PAGE_C.webp 2000w,
/docs/static/6cc23f597999ee52e128305c6621bd91/09625/NEW_HOME_PAGE_C.webp 3000w,
/docs/static/6cc23f597999ee52e128305c6621bd91/cddfd/NEW_HOME_PAGE_C.webp 3344w"
              sizes="(max-width: 2000px) 100vw, 2000px"
              type="image/webp"
            />
          <source
            srcset="/docs/static/6cc23f597999ee52e128305c6621bd91/b30f8/NEW_HOME_PAGE_C.png 500w,
/docs/static/6cc23f597999ee52e128305c6621bd91/332ff/NEW_HOME_PAGE_C.png 1000w,
/docs/static/6cc23f597999ee52e128305c6621bd91/99e71/NEW_HOME_PAGE_C.png 2000w,
/docs/static/6cc23f597999ee52e128305c6621bd91/22748/NEW_HOME_PAGE_C.png 3000w,
/docs/static/6cc23f597999ee52e128305c6621bd91/8c641/NEW_HOME_PAGE_C.png 3344w"
            sizes="(max-width: 2000px) 100vw, 2000px"
            type="image/png"
          />
          <img
            class="gatsby-resp-image-image"
            src="[./images/NEW_HOME_PAGE_C.png](https://raw.githubusercontent.com/marlonfrank30/f5-XCS-LB-WAAP-Policy-using-API-method/main/pictures/NEW_HOME_PAGE_C.webp)"
            alt="NEW HOME PAGE C"
            title="Figure: Homepage"
            loading="lazy"
            decoding="async"
            style="width:100%;height:100%;margin:0;vertical-align:middle;position:absolute;top:0;left:0;"
          />
        </picture>
    </span>
    <figcaption class="gatsby-resp-image-figcaption">Figure: Homepage</figcaption>
  </figure></p>
<ul>
<li>Select <code>Personal Management</code> in left column menu > select <code>Credentials</code> > <code>+ Create Credentials</code>.</li>
</ul>
<p><figure class="gatsby-resp-image-figure" style="">
    <span
      class="gatsby-resp-image-wrapper"
      style="position: relative; display: block; margin-left: auto; margin-right: auto; max-width: 2000px; "
    >
      <span
    class="gatsby-resp-image-background-image"
    style="padding-bottom: 53.2%; position: relative; bottom: 0; left: 0; background-image: url('data:image/webp;base64,UklGRjwAAABXRUJQVlA4IDAAAADQAgCdASoUAAsAPtFUo0uoJKMhsAgBABoJaQAAfj4AAP7yFO6hj89ihkQNSSVV4AA='); background-size: cover; display: block;"
  ></span>
  <picture>
          <source
              srcset="/docs/static/808dbc31857294917af65d54c0ff36b0/10636/CREDS_MAIN2.2B.webp 500w,
/docs/static/808dbc31857294917af65d54c0ff36b0/e00f7/CREDS_MAIN2.2B.webp 1000w,
/docs/static/808dbc31857294917af65d54c0ff36b0/56b60/CREDS_MAIN2.2B.webp 2000w,
/docs/static/808dbc31857294917af65d54c0ff36b0/09625/CREDS_MAIN2.2B.webp 3000w,
/docs/static/808dbc31857294917af65d54c0ff36b0/0c2e3/CREDS_MAIN2.2B.webp 3356w"
              sizes="(max-width: 2000px) 100vw, 2000px"
              type="image/webp"
            />
          <source
            srcset="/docs/static/808dbc31857294917af65d54c0ff36b0/b30f8/CREDS_MAIN2.2B.png 500w,
/docs/static/808dbc31857294917af65d54c0ff36b0/332ff/CREDS_MAIN2.2B.png 1000w,
/docs/static/808dbc31857294917af65d54c0ff36b0/99e71/CREDS_MAIN2.2B.png 2000w,
/docs/static/808dbc31857294917af65d54c0ff36b0/22748/CREDS_MAIN2.2B.png 3000w,
/docs/static/808dbc31857294917af65d54c0ff36b0/2c042/CREDS_MAIN2.2B.png 3356w"
            sizes="(max-width: 2000px) 100vw, 2000px"
            type="image/png"
          />
          <img
            class="gatsby-resp-image-image"
            src="/docs/static/808dbc31857294917af65d54c0ff36b0/99e71/CREDS_MAIN2.2B.png"
            alt="CREDS MAIN2 2B"
            title="Figure: Create Credentials"
            loading="lazy"
            decoding="async"
            style="width:100%;height:100%;margin:0;vertical-align:middle;position:absolute;top:0;left:0;"
          />
        </picture>
    </span>
    <figcaption class="gatsby-resp-image-figcaption">Figure: Create Credentials</figcaption>
  </figure></p>
</details>
<details>
<summary><b>Step 2:</b> Configure Credential type.</summary>  
<ul>
<li>
<p>Enter <code>Name</code> for your certificate.</p>
</li>
<li>
<p>Select <code>vK8s KubeConfig</code> in <code>Credential type</code> drop-down menu.</p>
</li>
<li>
<p>Select <code>Namespace</code> option in drop-down menu.</p>
</li>
<li>
<p>Select <code>vK8s cluster name</code> option in drop-down menu.</p>
</li>
<li>
<p>Select <code>Expiry date</code> from calendar drop-down.</p>
</li>
</ul>
<p><figure class="gatsby-resp-image-figure" style="">
    <span
      class="gatsby-resp-image-wrapper"
      style="position: relative; display: block; margin-left: auto; margin-right: auto; max-width: 2000px; "
    >
      <span
    class="gatsby-resp-image-background-image"
    style="padding-bottom: 53.2%; position: relative; bottom: 0; left: 0; background-image: url('data:image/webp;base64,UklGRkwAAABXRUJQVlA4IEAAAADwAgCdASoUAAsALplotFoiqCgoCACYSgC06COh1o5CtADWkPtRfCUGjuistzzpXc9xLVcGaUJ+j6mmz1UYYAAA'); background-size: cover; display: block;"
  ></span>
  <picture>
          <source
              srcset="/docs/static/cf0da2dd558d8e990e44aa7fae4df778/10636/CREDS_KUBECONFIG_3.webp 500w,
/docs/static/cf0da2dd558d8e990e44aa7fae4df778/e00f7/CREDS_KUBECONFIG_3.webp 1000w,
/docs/static/cf0da2dd558d8e990e44aa7fae4df778/56b60/CREDS_KUBECONFIG_3.webp 2000w,
/docs/static/cf0da2dd558d8e990e44aa7fae4df778/09625/CREDS_KUBECONFIG_3.webp 3000w,
/docs/static/cf0da2dd558d8e990e44aa7fae4df778/0c2e3/CREDS_KUBECONFIG_3.webp 3356w"
              sizes="(max-width: 2000px) 100vw, 2000px"
              type="image/webp"
            />
          <source
            srcset="/docs/static/cf0da2dd558d8e990e44aa7fae4df778/b30f8/CREDS_KUBECONFIG_3.png 500w,
/docs/static/cf0da2dd558d8e990e44aa7fae4df778/332ff/CREDS_KUBECONFIG_3.png 1000w,
/docs/static/cf0da2dd558d8e990e44aa7fae4df778/99e71/CREDS_KUBECONFIG_3.png 2000w,
/docs/static/cf0da2dd558d8e990e44aa7fae4df778/22748/CREDS_KUBECONFIG_3.png 3000w,
/docs/static/cf0da2dd558d8e990e44aa7fae4df778/2c042/CREDS_KUBECONFIG_3.png 3356w"
            sizes="(max-width: 2000px) 100vw, 2000px"
            type="image/png"
          />
          <img
            class="gatsby-resp-image-image"
            src="/docs/static/cf0da2dd558d8e990e44aa7fae4df778/99e71/CREDS_KUBECONFIG_3.png"
            alt="CREDS KUBECONFIG 3"
            title="Figure: Create vK8s KubeConfig"
            loading="lazy"
            decoding="async"
            style="width:100%;height:100%;margin:0;vertical-align:middle;position:absolute;top:0;left:0;"
          />
        </picture>
    </span>
    <figcaption class="gatsby-resp-image-figcaption">Figure: Create vK8s KubeConfig</figcaption>
  </figure></p>
</details>
<details>
<summary><b>Step 3:</b> Generate and download <code>vK8s KubeConfig</code> Certificate.</summary>
<ul>
<li>Select <code>Download</code> button to generate and download vK8s KubeConfig certificate file.</li>
</ul>
<p><figure class="gatsby-resp-image-figure" style="">
    <span
      class="gatsby-resp-image-wrapper"
      style="position: relative; display: block; margin-left: auto; margin-right: auto; max-width: 2000px; "
    >
      <span
    class="gatsby-resp-image-background-image"
    style="padding-bottom: 53.2%; position: relative; bottom: 0; left: 0; background-image: url('data:image/webp;base64,UklGRkwAAABXRUJQVlA4IEAAAADwAgCdASoUAAsALplotFoiqCgoCACYSgC06COh1o5CtADWkPtRfCUGjuistzzpXc9xLVcGaUJ+j6mmz1UYYAAA'); background-size: cover; display: block;"
  ></span>
  <picture>
          <source
              srcset="/docs/static/cf0da2dd558d8e990e44aa7fae4df778/10636/CREDS_KUBECONFIG_3.webp 500w,
/docs/static/cf0da2dd558d8e990e44aa7fae4df778/e00f7/CREDS_KUBECONFIG_3.webp 1000w,
/docs/static/cf0da2dd558d8e990e44aa7fae4df778/56b60/CREDS_KUBECONFIG_3.webp 2000w,
/docs/static/cf0da2dd558d8e990e44aa7fae4df778/09625/CREDS_KUBECONFIG_3.webp 3000w,
/docs/static/cf0da2dd558d8e990e44aa7fae4df778/0c2e3/CREDS_KUBECONFIG_3.webp 3356w"
              sizes="(max-width: 2000px) 100vw, 2000px"
              type="image/webp"
            />
          <source
            srcset="/docs/static/cf0da2dd558d8e990e44aa7fae4df778/b30f8/CREDS_KUBECONFIG_3.png 500w,
/docs/static/cf0da2dd558d8e990e44aa7fae4df778/332ff/CREDS_KUBECONFIG_3.png 1000w,
/docs/static/cf0da2dd558d8e990e44aa7fae4df778/99e71/CREDS_KUBECONFIG_3.png 2000w,
/docs/static/cf0da2dd558d8e990e44aa7fae4df778/22748/CREDS_KUBECONFIG_3.png 3000w,
/docs/static/cf0da2dd558d8e990e44aa7fae4df778/2c042/CREDS_KUBECONFIG_3.png 3356w"
            sizes="(max-width: 2000px) 100vw, 2000px"
            type="image/png"
          />
          <img
            class="gatsby-resp-image-image"
            src="/docs/static/cf0da2dd558d8e990e44aa7fae4df778/99e71/CREDS_KUBECONFIG_3.png"
            alt="CREDS KUBECONFIG 3"
            title="Figure: Generate and download vK8s KubeConfig Certificate"
            loading="lazy"
            decoding="async"
            style="width:100%;height:100%;margin:0;vertical-align:middle;position:absolute;top:0;left:0;"
          />
        </picture>
    </span>
    <figcaption class="gatsby-resp-image-figcaption">Figure: Generate and download vK8s KubeConfig Certificate</figcaption>
  </figure></p>
<blockquote>
<p><strong>Note</strong>: The maximum allowed expiry date for users is set by the tenant administrator. The system allows the administrator to set a maximum expiry of 365 days. The default expiry is 90 days.</p>
</blockquote>
<ul>
<li>Use in deployments after generating.</li>
</ul>
  </figure></p>
</details>


source: https://f5-amer-ent.console.ves.volterra.io/web/workspaces/administration/personal-management/api_credentials


<h2 id="prerequisites">Importing JSON into POSTMAN</h2>
To import the json file **F5 XCS Postman Collection.postman_collection.json** into Postman go under import  and then make necessary changes in the XCS Env Var to reflect your environemnt details such as tenant name, namespace, API cert and value, etc like the image below

![](./pictures/XCS%20ENV%20VAR.png)

now right click on the tasks and chosose to run all the tasks and watch for a 200 message back in the response header
![](./pictures/XCS%20ENV%20VAR2.png)
