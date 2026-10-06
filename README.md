<!--
  Profile README for github.com/Jahir509
  The stats, languages, streak and snake images live in ./profile and are rebuilt
  every day by .github/workflows/profile-stats.yml, so nothing here depends on
  rate-limited public card servers.
-->

# Jahir Ahmed

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://readme-typing-svg.demolab.com/?font=Barlow+Semi+Condensed&weight=600&size=26&duration=3200&pause=1400&color=5BC0BE&vCenter=true&width=760&height=44&lines=Backend+%26+platform+engineer;Early-warning+systems+for+cyclones%2C+floods+and+landslides;Python%2C+Django%2C+Node.js%2C+PostgreSQL%2C+Apache+Airflow;Self-hosted+Kubernetes%3A+RKE2+on+Proxmox">
  <img alt="Backend and platform engineer building early-warning systems for cyclones, floods and landslides" src="https://readme-typing-svg.demolab.com/?font=Barlow+Semi+Condensed&weight=600&size=26&duration=3200&pause=1400&color=0B3954&vCenter=true&width=760&height=44&lines=Backend+%26+platform+engineer;Early-warning+systems+for+cyclones%2C+floods+and+landslides;Python%2C+Django%2C+Node.js%2C+PostgreSQL%2C+Apache+Airflow;Self-hosted+Kubernetes%3A+RKE2+on+Proxmox">
</picture>

I build the backend side of early-warning systems: the pipelines that turn raw forecast models into rainfall, cyclone and landslide products, the APIs that publish them, and the self-hosted infrastructure underneath. I do it as a backend and platform engineer at [RIMES](https://www.rimes.int), a UN-registered intergovernmental organisation, for government agencies in Bangladesh, India and Timor-Leste.

The parts I care about most are the unglamorous ones: data that is actually correct, retries that make sense, and services that stay up when a cyclone is on its way.

<a href="mailto:me.jahirahmed@gmail.com"><img alt="Email me.jahirahmed@gmail.com" src="https://img.shields.io/badge/me.jahirahmed%40gmail.com-0B3954?style=flat-square&logo=gmail&logoColor=white"></a>
<a href="https://jahirahmed.com"><img alt="Website jahirahmed.com" src="https://img.shields.io/badge/jahirahmed.com-087E8B?style=flat-square&logo=googlechrome&logoColor=white"></a>
<img alt="Dhaka, Bangladesh, GMT+6" src="https://img.shields.io/badge/Dhaka%2C_Bangladesh-GMT%2B6-0B3954?style=flat-square">
<img alt="Profile views" src="https://komarev.com/ghpvc/?username=Jahir509&label=profile+views&color=087E8B&style=flat-square">
<!-- LinkedIn: replace YOUR-HANDLE, then move this line out of the comment
<a href="https://www.linkedin.com/in/YOUR-HANDLE"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square"></a>
-->

### By the numbers

<table>
  <tr>
    <td colspan="3" width="25%" valign="top">
      <h2>6+</h2>
      years shipping production backends, data pipelines and infrastructure
    </td>
    <td colspan="3" width="25%" valign="top">
      <h2>2</h2>
      of those years in Node.js, deploying to AWS EC2
    </td>
    <td colspan="3" width="25%" valign="top">
      <h2>3</h2>
      countries where government agencies use the data platforms I build and maintain: Bangladesh, India, Timor-Leste
    </td>
    <td colspan="3" width="25%" valign="top">
      <h2>5</h2>
      government agencies whose officials I have trained on-site, across 5 districts of Bangladesh
    </td>
  </tr>
  <!-- <tr>
    <td colspan="4" width="33%" valign="top">
      <h2>~6 days</h2>
      of lag removed from landslide hazard flags by fixing reversed rainfall weighting in our LHASA pipeline
    </td>
    <td colspan="4" width="33%" valign="top">
      <h2>~337 → ~12 mm</h2>
      a "24-hour" rainfall window that was quietly returning running totals instead of single-day values, caught and fixed
    </td>
    <td colspan="4" width="33%" valign="top">
      <h2>4 VIPs</h2>
      floated by one HAProxy + Keepalived pair across 2 self-hosted RKE2 clusters on 2 networks
    </td>
  </tr> -->
</table>

### Selected work

- **Forecast and warning APIs.** I maintain the Django/DRF APIs that serve processed forecast and warning products to [INSTANT](https://instant.bmd.gov.bd), other weather platforms, and [আবহাওয়া (Abohawa)](https://play.google.com/store/apps/details?id=bd.gov.bmd.abohawa), the Bangladesh Meteorological Department's official weather app. I also co-built, and now maintain, the weather-data processing behind them.
- **Cron to Apache Airflow 3.** Production DAGs for ECMWF 10 km and 25 km precipitation, BMD-WRF 9 km forecasts and the LHASA landslide model, running on a custom Docker image (CDO, NCO, rclone) with ntfy push alerts.
- **Getting the numbers right.** Five fixes in LHASA v1, including the reversed ARI weighting, a 2-day accumulation labelled as 7-day and an off-by-one hazard threshold, plus one shared rainfall-window module so the GeoJSON, GeoTIFF and PNG products agree.
- **TN-SMART.** About a year designing the Angular frontend architecture and building 6 modules for the Government of Tamil Nadu's multi-hazard alert and emergency-response platform.
- **Self-hosted Kubernetes.** RKE2 HA clusters on Proxmox and Rocky Linux: dual-network control planes behind HAProxy + Keepalived, Cilium with full kube-proxy replacement, and RKE2's CIS profile.
- **In the field.** Training and live demos for officials from the agriculture, livestock, fisheries, water and disaster-management departments (DAE, DLS, DoF, BWDB, DDM) in Patuakhali, Satkhira, Sylhet, Gaibandha and Chattogram.

**Background:** B.Sc. in Computer Science from United International University, and an Advanced Certificate for Management Professionals from IBA, University of Dhaka. Before RIMES: two years of Node.js development, Angular work, and QA on a core banking platform. Currently preparing for the CKA (Linux Foundation).

### Built in the open

| Project | What it does, and what it shows | Built with |
|---|---|---|
| **[chat-ai](https://github.com/Jahir509/chat-ai)**<br>[live demo](https://chat-ai.jahirahmed.com) | Multi-tenant chatbot platform: create agents, give them prompts and documents, get retrieval-grounded answers. Tenants are isolated at the query, prompt and retrieval layers (cross-tenant reads return 404, never 403), and LLM calls run outside database transactions so slow replies can't drain the connection pool. | Django 5.2, DRF, React 19, PostgreSQL 16, OpenAI Responses API, Caddy, Docker |
| **[web-relay](https://github.com/Jahir509/web-relay)** | Webhook delivery as a service. One transaction fans an event out to every subscriber; HMAC-signed requests get up to 8 attempts over ~28 hours with ±20% jitter; permanent failures go straight to a dead-letter queue you can replay. | FastAPI, PostgreSQL as the queue |
| **[ha-ticket-rush](https://github.com/Jahir509/ha-ticket-rush)**<br>+ [Django twin](https://github.com/Jahir509/ha-ticket-rush-django) | Flash-sale ticketing built to stress-test Kubernetes autoscaling (HPA): atomic Lua inventory decrements in Redis/Valkey, k6 load tests and Prometheus metrics. The sync Django twin drains orders into Postgres with batched `COPY`, so both execution models face the same load. | FastAPI, Django, Valkey, PostgreSQL, k6, Prometheus |
| **[hrm](https://github.com/Jahir509/hrm)** | Modular HR backend with one Django app per domain: leave, attendance, payroll, recruitment, performance. | Django, DRF |

### Right now

- Migrating cron-driven forecast pipelines into Apache Airflow 3
- Load-testing Ticket Rush on a single VM (async FastAPI vs sync Django) before taking it to Kubernetes
- Preparing for the Certified Kubernetes Administrator exam (Linux Foundation)
- Writing up how two RKE2 clusters share one HAProxy + Keepalived pair, for Medium
- Learning FastAPI in depth, Go, and agentic AI tooling

### Stack

<table>
  <tr>
    <td valign="top" width="150"><b>Backend</b></td>
    <td>
      <picture>
        <source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=py%2Cdjango%2Cfastapi%2Cpostgres%2Credis%2Crabbitmq%2Cnodejs%2Cexpress%2Cphp&theme=dark">
        <img alt="Python, Django, FastAPI, PostgreSQL, Redis, RabbitMQ, Node.js, Express, PHP" src="https://skillicons.dev/icons?i=py%2Cdjango%2Cfastapi%2Cpostgres%2Credis%2Crabbitmq%2Cnodejs%2Cexpress%2Cphp&theme=light">
      </picture>
      <br>
      <img alt="Django REST Framework" src="https://img.shields.io/badge/Django_REST_Framework-A30000?style=flat-square&logo=django&logoColor=white">
      <img alt="Celery" src="https://img.shields.io/badge/Celery-37814A?style=flat-square&logo=celery&logoColor=white">
      <img alt="Gunicorn" src="https://img.shields.io/badge/Gunicorn-499848?style=flat-square&logo=gunicorn&logoColor=white">
      <img alt="CodeIgniter" src="https://img.shields.io/badge/CodeIgniter-EF4223?style=flat-square&logo=codeigniter&logoColor=white">
    </td>
  </tr>
  <tr>
    <td valign="top"><b>Data and geospatial</b></td>
    <td>
      <img alt="Apache Airflow" src="https://img.shields.io/badge/Apache_Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white">
      <img alt="pandas" src="https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white">
      <img alt="GeoPandas" src="https://img.shields.io/badge/GeoPandas-0B3954?style=flat-square">
      <img alt="rasterio" src="https://img.shields.io/badge/rasterio-0B3954?style=flat-square">
      <img alt="NetCDF" src="https://img.shields.io/badge/NetCDF-0B3954?style=flat-square">
      <img alt="PostGIS" src="https://img.shields.io/badge/PostGIS-0B3954?style=flat-square">
      <img alt="WRF and ECMWF model output" src="https://img.shields.io/badge/WRF_%2F_ECMWF_output-0B3954?style=flat-square">
      <img alt="Leaflet" src="https://img.shields.io/badge/Leaflet-199900?style=flat-square&logo=leaflet&logoColor=white">
      <img alt="Mapbox" src="https://img.shields.io/badge/Mapbox-000000?style=flat-square&logo=mapbox&logoColor=white">
      <img alt="Turf.js" src="https://img.shields.io/badge/Turf.js-0B3954?style=flat-square">
    </td>
  </tr>
  <tr>
    <td valign="top"><b>Platform</b></td>
    <td>
      <picture>
        <source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=docker%2Ckubernetes%2Clinux%2Credhat%2Cubuntu%2Cnginx%2Cjenkins%2Cprometheus%2Caws%2Cbash%2Cgit&theme=dark">
        <img alt="Docker, Kubernetes, Linux, Red Hat, Ubuntu, Nginx, Jenkins, Prometheus, AWS, Bash, Git" src="https://skillicons.dev/icons?i=docker%2Ckubernetes%2Clinux%2Credhat%2Cubuntu%2Cnginx%2Cjenkins%2Cprometheus%2Caws%2Cbash%2Cgit&theme=light">
      </picture>
      <br>
      <img alt="RKE2" src="https://img.shields.io/badge/RKE2-0075A8?style=flat-square&logo=rancher&logoColor=white">
      <img alt="Cilium" src="https://img.shields.io/badge/Cilium-F8C517?style=flat-square&logo=cilium&logoColor=black">
      <img alt="HAProxy and Keepalived" src="https://img.shields.io/badge/HAProxy_%2B_Keepalived-0B3954?style=flat-square">
      <img alt="Proxmox" src="https://img.shields.io/badge/Proxmox-E57000?style=flat-square&logo=proxmox&logoColor=white">
      <img alt="Rocky Linux" src="https://img.shields.io/badge/Rocky_Linux-10B981?style=flat-square&logo=rockylinux&logoColor=white">
      <img alt="k6" src="https://img.shields.io/badge/k6-7D64FF?style=flat-square&logo=k6&logoColor=white">
    </td>
  </tr>
  <tr>
    <td valign="top"><b>Frontend</b></td>
    <td>
      <picture>
        <source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=angular%2Cts%2Cjs%2Creact%2Ctailwind%2Cvite&theme=dark">
        <img alt="Angular, TypeScript, JavaScript, React, Tailwind CSS, Vite" src="https://skillicons.dev/icons?i=angular%2Cts%2Cjs%2Creact%2Ctailwind%2Cvite&theme=light">
      </picture>
    </td>
  </tr>
  <tr>
    <td valign="top"><b>Also shipped with</b></td>
    <td>
      <picture>
        <source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=cs%2Cdotnet%2Cmysql%2Cmongodb%2Claravel%2Cpostman&theme=dark">
        <img alt="C#, .NET, MySQL, MongoDB, Laravel, Postman" src="https://skillicons.dev/icons?i=cs%2Cdotnet%2Cmysql%2Cmongodb%2Claravel%2Cpostman&theme=light">
      </picture>
    </td>
  </tr>
</table>

### On GitHub

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Jahir509/Jahir509/main/profile/stats-dark.svg">
  <img alt="GitHub stats for Jahir509" src="https://raw.githubusercontent.com/Jahir509/Jahir509/main/profile/stats.svg" height="150">
</picture>
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Jahir509/Jahir509/main/profile/top-langs-dark.svg">
  <img alt="Languages across Jahir509's public repositories" src="https://raw.githubusercontent.com/Jahir509/Jahir509/main/profile/top-langs.svg" height="150">
</picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Jahir509/Jahir509/main/profile/streak-dark.svg">
  <img alt="Contribution streak for Jahir509" src="https://raw.githubusercontent.com/Jahir509/Jahir509/main/profile/streak.svg">
</picture>

### Get in touch

Open to remote backend and platform roles and to open-source collaboration. Always happy to talk Django, Node.js, Angular, Airflow, PostgreSQL, or running Kubernetes on your own hardware. Email is the fastest way to reach me: [me.jahirahmed@gmail.com](mailto:me.jahirahmed@gmail.com)

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Jahir509/Jahir509/main/profile/snake-dark.svg">
  <img alt="A snake eating Jahir509's contribution graph" src="https://raw.githubusercontent.com/Jahir509/Jahir509/main/profile/snake.svg">
</picture>
