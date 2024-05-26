# IPL Dashboard App

In this project, I have built an **IPL Dashboard App** by applying the concepts I have learned till now.

### Refer to the image below: 

<br/>
<div style="text-align: center;">
    <img src="https://assets.ccbp.in/frontend/content/react-js/ipl-dashboard-output-v2.gif" alt="ipl-dashboard-output" style="max-width:70%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12)">
</div>
<br/>

### Design Files

<details>
<summary>Click to view</summary>

- [Extra Small (Size < 576px) and Small (Size >= 576px) - Home](https://assets.ccbp.in/frontend/content/react-js/ipl-dashboard-home-sm-output.png)
- [Extra Small (Size < 576px) and Small (Size >= 576px) - Team Matches](https://assets.ccbp.in/frontend/content/react-js/ipl-dashboard-team-matches-sm-output-v2.png)
- [Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px) - Home](https://assets.ccbp.in/frontend/content/react-js/ipl-dashboard-home-lg-output.png)
- [Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px) - Team Matches](https://assets.ccbp.in/frontend/content/react-js/ipl-dashboard-team-matches-lg-output-v2.png)

</details>

### Set Up Instructions

<details>
<summary>Click to view</summary>

- Download dependencies by running `npm install`
- Start up the app using `npm start`
</details>

### API Requests & Responses

<details>
<summary>Click to view</summary>

**teamsApiUrl**

#### API: `https://apis.ccbp.in/ipl`

#### Method: `GET`

#### Description:

Returns a response containing the list of all IPL teams

#### Response

```json
{
  "teams": [
    {
      "name": "Royal Challengers Bangalore",
      "id": "RCB",
      "team_image_url": "https://assets.ccbp.in/frontend/react-js/rcb-logo-img.png",
      // use value of the key 'name' for alt as `${name}`
    },
    ...
  ],
}
```

**teamMatchesApiUrl**

#### API: `https://apis.ccbp.in/ipl/:id`

#### Example: `https://apis.ccbp.in/ipl/KKR`

#### Method: `GET`

#### Description:

Returns a response containing details of all recent matches of a team

#### Response

```json
{
  "team_banner_url": "https://assets.ccbp.in/frontend/react-js/kkr-team-img.png",
  "latest_match_details": {
    "umpires": "CB Gaffaney, VK Sharma",
    "result": "Kolkata Knight Riders Won by 7 wickets",
    "man_of_the_match": "Shubman Gill",
    "id": "1216545",
    "date": "2020-09-26",
    "venue": "At Sheikh Zayed Stadium, Abu Dhabi",
    "competing_team": "Sunrisers Hyderabad",
    "competing_team_logo": "https://upload.wikimedia.org/wikipedia/en/thumb/8/81/Sunrisers_Hyderabad.svg/1200px-Sunrisers_Hyderabad.svg.png",
    // use value of the key 'competing_team' for alt as `latest match ${competing_team}`
    "first_innings": "Sunrisers Hyderabad",
    "second_innings": "Kolkata Knight Riders",
    "match_status": "Won",
  },
  "recent_matches": [
    {
      "umpires": "RK Illingworth, K Srinivasan",
      "result": "Royal Challengers Bangalore Won by 82 runs",
      "man_of_the_match": "AB de Villiers",
      "id": "1216540",
      "date": "2020-10-12",
      "venue": "At Sharjah Cricket Stadium, Sharjah",
      "competing_team": "Royal Challengers Bangalore",
      "competing_team_logo": "https://upload.wikimedia.org/wikipedia/en/thumb/2/2a/Royal_Challengers_Bangalore_2020.svg/1200px-Royal_Challengers_Bangalore_2020.svg.png",
      // use value of the key 'competing_team' for alt as `competing team ${competing_team}`
      "first_innings": "Royal Challengers Bangalore",
      "second_innings": "Kolkata Knight Riders",
      "match_status": "Lost",
    },
    ...
  ],
}
```

</details>

### Components Structure

<details>
<summary>Click to view</summary>

<br/>
<div style="text-align: center;">
    <img src="https://assets.ccbp.in/frontend/content/react-js/home-component-structure-img.png" alt="home component structure" style="max-width:100%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12)">
</div>
<br/>

<div style="text-align: center;">
    <img src="https://assets.ccbp.in/frontend/content/react-js/team-matches-component-structure-img.png" alt="team matches component structure" style="max-width:100%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12)">
</div>
<br/>

</details>

### Implementation Files

<details>
<summary>Click to view</summary>
<br/>

Use these files to complete the implementation:

- `src/App.js`
- `src/components/Home/index.js`
- `src/components/Home/index.css`
- `src/components/TeamCard/index.js`
- `src/components/TeamCard/index.css`
- `src/components/TeamMatches/index.js`
- `src/components/TeamMatches/index.css`
- `src/components/LatestMatch/index.js`
- `src/components/LatestMatch/index.css`
- `src/components/MatchCard/index.js`
- `src/components/MatchCard/index.css`
</details>

### Resources

<details>
<summary>Image URLs</summary>

- [https://assets.ccbp.in/frontend/react-js/ipl-dashboard-sm-bg.png](https://assets.ccbp.in/frontend/react-js/ipl-dashboard-sm-bg.png)
- [https://assets.ccbp.in/frontend/react-js/ipl-dashboard-lg-bg.png](https://assets.ccbp.in/frontend/react-js/ipl-dashboard-lg-bg.png)
- [https://assets.ccbp.in/frontend/react-js/ipl-logo-img.png](https://assets.ccbp.in/frontend/react-js/ipl-logo-img.png) alt should be **ipl logo**

</details>

<details>
<summary>Colors</summary>

<br/>

**Background Colors**:

<div style="background-color: #1e293b; width: 150px; padding: 10px; color: white">Hex: #1e293b</div>
<div style="background-color: #a4261d; width: 150px; padding: 10px; color: white">Hex: #a4261d</div>
<div style="background-color: #5755a7; width: 150px; padding: 10px; color: white">Hex: #5755a7</div>
<div style="background-color: #d91c1f; width: 150px; padding: 10px; color: white">Hex: #d91c1f</div>
<div style="background-color: #f7db00; width: 150px; padding: 10px; color: white">Hex: #f7db00</div>
<div style="background-color: #ffffff33; width: 150px; padding: 10px; color: black">Hex: #ffffff33</div>

</details>

<details>
<summary>Font-families</summary>

- Bree Serif

</details>
