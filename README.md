# fhem

Base Repository for my private modules i did for my personal use.<br />
<b>Caution!! They may be dangerous and crash your fhem instance!</b>


<h3>SolarEdge API</h3>
<ul>
    <u><b>SolarEdge API - Retrieves data from the SolarEdge Monitoring API</b></u>
    <br>
    With this module it is possible to read the data from a SolarEdge PV and to set it as reading.
    <br><br>
    <a name="SolarEdgeAPIdefine"></a>
    <b>Define</b>
    <ul><br>
        <code>define &lt;name&gt; SolarEdgeAPI &lt;API-Key&gt; &lt;SiteId&gt;</code>
    <br><br>
    Example:
    <ul><br>
        <code>define myPVSite SolarEdgeAPI ABC123 123456</code><br>
    </ul>
    <br>
    This statement creates a Device with the name myPV using API-Key ABC123 for fetching data of Site-Id 123456<br>
    After the device has been created, the current data of the site is automatically read from the API.
    The API-Key has to be enabled in the "Admin" Section of the Monitoring-Portal. There you can find your Site-ID, too.
    According to the docs there is a limit of 300 total requests per day.
    </ul>
    <br><br>
    <a name="SolarEdgeAPIreadings"></a>
    <b>Readings</b>
    <ul>
        <li>actionQueue     - information about the entries in the action queue</li>
        <li>aggregates-*    - cumulative data of the energyDetails response</li>
        <li>status-*        - readings of the currentPowerFlow response</li>
    </ul>
    <a name="SolarEdgeAPIget"></a>
    <b>get</b>
    <ul>
        <li>aggregates      - fetch data from energyDetails.json</li>
        <li>status          - fetch data currentPowerFlow.json </li>
    </ul>
    <a name="SolarEdgeAPIattribute"></a>
    <b>Attribute</b>
    <ul>
        <li>interval - interval in seconds for automatically fetch data (default auto = 300 (sec) daytime and 1200 (sec) nighttime)</li>
    </ul>
</ul>
