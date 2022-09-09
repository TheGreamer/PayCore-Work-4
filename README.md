<i>🌟 PayCore .NET Core Bootcamp - 4th Week</i>

<hr />
<h2>🧐 About The Project</h2>
<ul>
    <li>An ASP.NET Web API project developed with .NET 6.</li>
    <li>The explanations about the classes and the features they contain were detailed in the comment lines in each file</li>
    <li><a href="https://www.postgresql.org" target="_blank">PostgreSQL</a> database was used.</li>
    <li><a href="https://nhibernate.info" target="_blank">NHibernate</a> ORM tool was used.</li>
    <li>An example result is at the bottom of this page.</li>
    <li>The script codes of the database can be accessed from <a href="https://pastebin.com/pk7mtrZz" target="_blank">this link</a>. (VPN may be required.)</li>
    <li>Traveling salesman algorithm was inspired. Mathematical formulas were used for distance calculation.</li>
    <li>A helper model class was used in the creation of the method used in clustering operations.</li>
</ul>

<hr />
<h2>💻 Project Structure</h2>
<ul>
    <li>Controllers
        <ul>
            <li><a href="https://github.com/TheGreamer/PayCore-Work-4/blob/main/PayCoreClassWork4/PayCoreClassWork4/Controllers/ClusteringController.cs">ClusteringController.cs</a></li>
        </ul>
    </li>
    <li>Extensions
        <ul>
            <li><a href="https://github.com/TheGreamer/PayCore-Work-4/blob/main/PayCoreClassWork4/PayCoreClassWork4/Extensions/NHibernateExtension.cs">NHibernateExtension.cs</a></li>
        </ul>
    </li>
    <li>Models
        <ul>
            <li><a href="https://github.com/TheGreamer/PayCore-Work-4/blob/main/PayCoreClassWork4/PayCoreClassWork4/Models/Vehicle.cs">Vehicle.cs</a></li>
            <li><a href="https://github.com/TheGreamer/PayCore-Work-4/blob/main/PayCoreClassWork4/PayCoreClassWork4/Models/Container.cs">Container.cs</a></li>
            <li><a href="https://github.com/TheGreamer/PayCore-Work-4/blob/main/PayCoreClassWork4/PayCoreClassWork4/Models/ContainersWithDistance.cs">ContainersWithDistance.cs</a></li>
        </ul>
    </li>
    <li>Mappings
        <ul>
            <li><a href="https://github.com/TheGreamer/PayCore-Work-4/blob/main/PayCoreClassWork4/PayCoreClassWork4/Mappings/VehicleMap.cs">VehicleMap.cs</a></li>
            <li><a href="https://github.com/TheGreamer/PayCore-Work-4/blob/main/PayCoreClassWork4/PayCoreClassWork4/Mappings/ContainerMap.cs">ContainerMap.cs</a></li>
        </ul>
    </li>
    <li>Utilities
        <ul>
            <li><a href="https://github.com/TheGreamer/PayCore-Work-4/blob/main/PayCoreClassWork4/PayCoreClassWork4/Utilities/Calculation.cs">Calculation.cs</a></li>
        </ul>
    </li>
    <li><a href="https://github.com/TheGreamer/PayCore-Work-4/blob/main/PayCoreClassWork4/PayCoreClassWork4/Program.cs">Program.cs</a></li>
    <li><a href="https://github.com/TheGreamer/PayCore-Work-4/blob/main/PayCoreClassWork4/PayCoreClassWork4/appsettings.json">appsettings.json</a></li>
</ul>

<hr />
<h2><b>📒 Database Table and Column Presentation</b></h2>
<ul>
    <li>
        <h3>🌟 Vehicle Table</h3>
        <p dir="auto">
            <a target="_blank" rel="noopener noreferrer" href="">
                <img src="https://i.hizliresim.com/92c310o.png" alt="Swagger" style="max-width: 100%;">
            </a>
        </p>
    </li>
    <li>
        <h3>🌟 Container Table</h3>
        <p dir="auto">
            <a target="_blank" rel="noopener noreferrer" href="">
                <img src="https://i.hizliresim.com/3nrvd5f.png" alt="Swagger" style="max-width: 100%;">
            </a>
        </p>
    </li>
</ul>

<hr />
<h2><b>🌟 Result</b></h2>
<h4>Example: There are 8 (N) vehicles with vehicle number 1(id) in the database. The sample JSON output of the list of lists formed when it is aimed to fill and discharge over the shortest distance by clustering in 3 (X) different routes is as follows.</h4>
<br />
<code>[HttpGet("{vehicleId}/{clusterCount}")] Get(long? vehicleId, int? clusterCount)</code>
<br />
<code>Request URL: api/Clustering/1/3</code>
<br />
<br />

```JSON
[
  [
    {
      "containers": [
        {
          "id": 3,
          "containerName": "TestContainer3",
          "latitude": 33.235214,
          "longitude": 40.331585,
          "vehicleId": 1
        },
        {
          "id": 4,
          "containerName": "TestContainer4",
          "latitude": 32.235214,
          "longitude": 39.331585,
          "vehicleId": 1
        }
      ],
      "distance": 145.3014335758858
    },
    {
      "containers": [
        {
          "id": 4,
          "containerName": "TestContainer4",
          "latitude": 32.235214,
          "longitude": 39.331585,
          "vehicleId": 1
        },
        {
          "id": 5,
          "containerName": "TestContainer5",
          "latitude": 31.235214,
          "longitude": 38.331585,
          "vehicleId": 1
        }
      ],
      "distance": 145.9699859772582
    },
    {
      "containers": [
        {
          "id": 5,
          "containerName": "TestContainer5",
          "latitude": 31.235214,
          "longitude": 38.331585,
          "vehicleId": 1
        },
        {
          "id": 6,
          "containerName": "TestContainer6",
          "latitude": 30.235214,
          "longitude": 37.331585,
          "vehicleId": 1
        }
      ],
      "distance": 146.62401820541245
    }
  ],
  [
    {
      "containers": [
        {
          "id": 6,
          "containerName": "TestContainer6",
          "latitude": 30.235214,
          "longitude": 37.331585,
          "vehicleId": 1
        },
        {
          "id": 7,
          "containerName": "TestContainer7",
          "latitude": 29.235214,
          "longitude": 36.331585,
          "vehicleId": 1
        }
      ],
      "distance": 147.26293208619572
    },
    {
      "containers": [
        {
          "id": 7,
          "containerName": "TestContainer7",
          "latitude": 29.235214,
          "longitude": 36.331585,
          "vehicleId": 1
        },
        {
          "id": 8,
          "containerName": "TestContainer8",
          "latitude": 28.235214,
          "longitude": 35.331585,
          "vehicleId": 1
        }
      ],
      "distance": 147.88615008326633
    },
    {
      "containers": [
        {
          "id": 1,
          "containerName": "TestContainer1",
          "latitude": 35.235214,
          "longitude": 42.331585,
          "vehicleId": 1
        },
        {
          "id": 3,
          "containerName": "TestContainer3",
          "latitude": 33.235214,
          "longitude": 40.331585,
          "vehicleId": 1
        }
      ],
      "distance": 288.5334071608722
    }
  ],
  [
    {
      "containers": [
        {
          "id": 8,
          "containerName": "TestContainer8",
          "latitude": 28.235214,
          "longitude": 35.331585,
          "vehicleId": 1
        },
        {
          "id": 2,
          "containerName": "TestContainer2",
          "latitude": 34.235214,
          "longitude": 41.331585,
          "vehicleId": 1
        }
      ],
      "distance": 877.4020546726479
    }
  ]
]
```
