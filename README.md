<header>

<!--
  <<< Author notes: Course header >>>
  Include a 1280×640 image, course title in sentence case, and a concise description in emphasis.
  In your repository settings: enable template repository, add your 1280×640 social image, auto delete head branches.
  Add your open source license, GitHub uses MIT license.
-->

# GitHub Pages

_Create a site or blog from your GitHub repositories with GitHub Pages._

</header>

<!--
  <<< Author notes: Step 1 >>>
  Choose 3-5 steps for your course.
  The first step is always the hardest, so pick something easy!
  Link to docs.github.com for further explanations.
  Encourage users to open new tabs for steps!
-->

## Step 1: Enable GitHub Pages

_Welcome to GitHub Pages and Jekyll :tada:!_

The first step is to enable GitHub Pages on this [repository](https://docs.github.com/en/get-started/quickstart/github-glossary#repository). When you enable GitHub Pages on a repository, GitHub takes the content that's on the main branch and publishes a website based on its contents.

### :keyboard: Activity: Enable GitHub Pages

1. Open a new browser tab, and work on the steps in your second tab while you read the instructions in this tab.
1. Under your repository name, click **Settings**.
1. Click **Pages** in the **Code and automation** section.
1. Ensure "Deploy from a branch" is selected from the **Source** drop-down menu, and then select `main` from the **Branch** drop-down menu.
1. Click the **Save** button.
1. Wait about _one minute_ then refresh this page (the one you're following instructions from). [GitHub Actions](https://docs.github.com/en/actions) will automatically update to the next step.
   > Turning on GitHub Pages creates a deployment of your repository. GitHub Actions may take up to a minute to respond while waiting for the deployment. Future steps will be about 20 seconds; this step is slower.
   > **Note**: In the **Pages** of **Settings**, the **Visit site** button will appear at the top. Click the button to see your GitHub Pages site.

<footer>

<!--
  <<< Author notes: Footer >>>
  Add a link to get support, GitHub status page, code of conduct, license link.
-->

---

Get help: [Post in our discussion board](https://github.com/orgs/skills/discussions/categories/github-pages) &bull; [Review the GitHub status page](https://www.githubstatus.com/)

&copy; 2023 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)

</footer>
<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mapa de Calor</title>
    <style>
        html, body {
            height: 100%;
            margin: 0;
            padding: 0;
            overflow: hidden;
        }
        #map {
            width: 100%;
            height: 100vh;
        }
    </style>
    <script src="https://maps.googleapis.com/maps/api/js?key=SUA_CHAVE_API_AQUI&libraries=visualization"></script>
    <script>
        function initMap() {
            var map = new google.maps.Map(document.getElementById('map'), {
                center: { lat: -5.491954, lng: -47.483348 },
                zoom: 15,
                mapTypeId: 'satellite'
            });

            var heatmapData = [
                { location: new google.maps.LatLng(-5.491954, -47.483348), weight: 1 },
                { location: new google.maps.LatLng(-5.530347, -47.491044), weight: 1 },
                { location: new google.maps.LatLng(-5.528214, -47.475979), weight: 1 },
                { location: new google.maps.LatLng(-5.473788, -47.526276), weight: 1 },
                { location: new google.maps.LatLng(-5.528389, -47.473766), weight: 1 },
                { location: new google.maps.LatLng(-5.524271, -47.474949), weight: 1 },
                { location: new google.maps.LatLng(-5.500147, -47.486535), weight: 1 },
                { location: new google.maps.LatLng(-5.648722, -47.397472), weight: 1 },
                { location: new google.maps.LatLng(-5.509771, -47.488400), weight: 1 },
                { location: new google.maps.LatLng(-5.482375, -47.487905), weight: 1 },
                { location: new google.maps.LatLng(-5.507541, -47.500990), weight: 1 },
                { location: new google.maps.LatLng(-5.562647, -47.451923), weight: 1 },
                { location: new google.maps.LatLng(-5.489960, -47.486296), weight: 1 },
                { location: new google.maps.LatLng(-5.505709, -47.487612), weight: 1 },
                { location: new google.maps.LatLng(-5.506165, -47.488419), weight: 1 },
                { location: new google.maps.LatLng(-5.509177, -47.487142), weight: 1 },
                { location: new google.maps.LatLng(-5.491629, -47.483848), weight: 1 },
                { location: new google.maps.LatLng(-5.735687, -47.359803), weight: 1 },
                { location: new google.maps.LatLng(-5.540608, -47.486952), weight: 1 },
                { location: new google.maps.LatLng(-5.483180, -47.474596), weight: 1 },
                { location: new google.maps.LatLng(-5.337407, -47.595294), weight: 1 },
                { location: new google.maps.LatLng(-5.541337, -47.471847), weight: 1 },
                { location: new google.maps.LatLng(-5.492683, -47.484930), weight: 1 },
                { location: new google.maps.LatLng(-5.540075, -47.486291), weight: 1 },
                { location: new google.maps.LatLng(-5.502055, -47.486519), weight: 1 },
                { location: new google.maps.LatLng(-5.527625, -47.476445), weight: 1 },
                { location: new google.maps.LatLng(-5.527919, -47.471842), weight: 1 },
                { location: new google.maps.LatLng(-5.522041, -47.481237), weight: 1 },
                { location: new google.maps.LatLng(-5.535580, -47.488664), weight: 1 },
                { location: new google.maps.LatLng(-5.273047, -47.517335), weight: 1 },
                { location: new google.maps.LatLng(-5.480861, -47.482266), weight: 1 },
                { location: new google.maps.LatLng(-5.543818, -47.488131), weight: 1 },
                { location: new google.maps.LatLng(-5.481084, -47.488635), weight: 1 },
                { location: new google.maps.LatLng(-5.530454, -47.478873), weight: 1 },
                { location: new google.maps.LatLng(-5.512845, -47.484317), weight: 1 },
                { location: new google.maps.LatLng(-5.524054, -47.492018), weight: 1 },
                { location: new google.maps.LatLng(-5.489930, -47.482172), weight: 1 },
                { location: new google.maps.LatLng(-5.498021, -47.485542), weight: 1 },
                { location: new google.maps.LatLng(-5.491541, -47.489479), weight: 1 },
                { location: new google.maps.LatLng(-5.528524, -47.476346), weight: 1 },
                { location: new google.maps.LatLng(-5.530007, -47.493140), weight: 1 },
                { location: new google.maps.LatLng(-5.652419, -47.395133), weight: 1 },
                { location: new google.maps.LatLng(-5.529141, -47.472170), weight: 1 },
                { location: new google.maps.LatLng(-5.530805, -47.480684), weight: 1 },
                { location: new google.maps.LatLng(-5.534438, -47.486744), weight: 1 },
                { location: new google.maps.LatLng(-5.566961, -47.460462), weight: 1 },
                { location: new google.maps.LatLng(-5.475726, -47.525010), weight: 1 },
                { location: new google.maps.LatLng(-5.471540, -47.524342), weight: 1 },
                { location: new google.maps.LatLng(-5.747878, -47.363345), weight: 1 },
                { location: new google.maps.LatLng(-5.740608, -47.374161), weight: 1 },
                { location: new google.maps.LatLng(-5.506381, -47.487200), weight: 1 },
                { location: new google.maps.LatLng(-5.543329, -47.488101), weight: 1 }
            ];

            var heatmap = new google.maps.visualization.HeatmapLayer({
                data: heatmapData,
                radius: 30
            });

            heatmap.setMap(map);
        }
    </script>
</head>
<body onload="initMap()">
    <div id="map"></div>
</body>
</html>
<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mapa de Calor</title>
    <style>
        html, body {
            height: 100%;
            margin: 0;
            padding: 0;
            overflow: hidden;
        }
        #map {
            width: 100%;
            height: 100vh;
        }
    </style>
    <script src="https://maps.googleapis.com/maps/api/js?key=SUA_CHAVE_API_AQUI&libraries=visualization"></script>
    <script>
        function initMap() {
            var map = new google.maps.Map(document.getElementById('map'), {
                center: { lat: -5.491954, lng: -47.483348 },
                zoom: 15,
                mapTypeId: 'satellite'
            });

            var heatmapData = [
                { location: new google.maps.LatLng(-5.491954, -47.483348), weight: 1 },
                { location: new google.maps.LatLng(-5.530347, -47.491044), weight: 1 },
                { location: new google.maps.LatLng(-5.528214, -47.475979), weight: 1 },
                { location: new google.maps.LatLng(-5.473788, -47.526276), weight: 1 },
                { location: new google.maps.LatLng(-5.528389, -47.473766), weight: 1 },
                { location: new google.maps.LatLng(-5.524271, -47.474949), weight: 1 },
                { location: new google.maps.LatLng(-5.500147, -47.486535), weight: 1 },
                { location: new google.maps.LatLng(-5.648722, -47.397472), weight: 1 },
                { location: new google.maps.LatLng(-5.509771, -47.488400), weight: 1 },
                { location: new google.maps.LatLng(-5.482375, -47.487905), weight: 1 },
                { location: new google.maps.LatLng(-5.507541, -47.500990), weight: 1 },
                { location: new google.maps.LatLng(-5.562647, -47.451923), weight: 1 },
                { location: new google.maps.LatLng(-5.489960, -47.486296), weight: 1 },
                { location: new google.maps.LatLng(-5.505709, -47.487612), weight: 1 },
                { location: new google.maps.LatLng(-5.506165, -47.488419), weight: 1 },
                { location: new google.maps.LatLng(-5.509177, -47.487142), weight: 1 },
                { location: new google.maps.LatLng(-5.491629, -47.483848), weight: 1 },
                { location: new google.maps.LatLng(-5.735687, -47.359803), weight: 1 },
                { location: new google.maps.LatLng(-5.540608, -47.486952), weight: 1 },
                { location: new google.maps.LatLng(-5.483180, -47.474596), weight: 1 },
                { location: new google.maps.LatLng(-5.337407, -47.595294), weight: 1 },
                { location: new google.maps.LatLng(-5.541337, -47.471847), weight: 1 },
                { location: new google.maps.LatLng(-5.492683, -47.484930), weight: 1 },
                { location: new google.maps.LatLng(-5.540075, -47.486291), weight: 1 },
                { location: new google.maps.LatLng(-5.502055, -47.486519), weight: 1 },
                { location: new google.maps.LatLng(-5.527625, -47.476445), weight: 1 },
                { location: new google.maps.LatLng(-5.527919, -47.471842), weight: 1 },
                { location: new google.maps.LatLng(-5.522041, -47.481237), weight: 1 },
                { location: new google.maps.LatLng(-5.535580, -47.488664), weight: 1 },
                { location: new google.maps.LatLng(-5.273047, -47.517335), weight: 1 },
                { location: new google.maps.LatLng(-5.480861, -47.482266), weight: 1 },
                { location: new google.maps.LatLng(-5.543818, -47.488131), weight: 1 },
                { location: new google.maps.LatLng(-5.481084, -47.488635), weight: 1 },
                { location: new google.maps.LatLng(-5.530454, -47.478873), weight: 1 },
                { location: new google.maps.LatLng(-5.512845, -47.484317), weight: 1 },
                { location: new google.maps.LatLng(-5.524054, -47.492018), weight: 1 },
                { location: new google.maps.LatLng(-5.489930, -47.482172), weight: 1 },
                { location: new google.maps.LatLng(-5.498021, -47.485542), weight: 1 },
                { location: new google.maps.LatLng(-5.491541, -47.489479), weight: 1 },
                { location: new google.maps.LatLng(-5.528524, -47.476346), weight: 1 },
                { location: new google.maps.LatLng(-5.530007, -47.493140), weight: 1 },
                { location: new google.maps.LatLng(-5.652419, -47.395133), weight: 1 },
                { location: new google.maps.LatLng(-5.529141, -47.472170), weight: 1 },
                { location: new google.maps.LatLng(-5.530805, -47.480684), weight: 1 },
                { location: new google.maps.LatLng(-5.534438, -47.486744), weight: 1 },
                { location: new google.maps.LatLng(-5.566961, -47.460462), weight: 1 },
                { location: new google.maps.LatLng(-5.475726, -47.525010), weight: 1 },
                { location: new google.maps.LatLng(-5.471540, -47.524342), weight: 1 },
                { location: new google.maps.LatLng(-5.747878, -47.363345), weight: 1 },
                { location: new google.maps.LatLng(-5.740608, -47.374161), weight: 1 },
                { location: new google.maps.LatLng(-5.506381, -47.487200), weight: 1 },
                { location: new google.maps.LatLng(-5.543329, -47.488101), weight: 1 }
            ];

            var heatmap = new google.maps.visualization.HeatmapLayer({
                data: heatmapData,
                radius: 30
            });

            heatmap.setMap(map);
        }
    </script>
</head>
<body onload="initMap()">
    <div id="map"></div>
</body>
</html>
