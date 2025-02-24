### Node Preview 

![image](https://github.com/codereport/city-strides-hacking/assets/36027403/ef99afe0-82e4-49a1-9358-1b741179635b)

### Route Generation

![image](https://github.com/codereport/city-strides-hacking/assets/36027403/ae71254c-8f82-40ba-9a7a-ac5811ee005b)

# How to Use the Python Scripts

1. `git clone https://github.com/codereport/city-strides-hacking.git`

2. Add a file named `cookies.json` with the following contents:

```json
{
    "_citystrides_session": "...",
    "remember_user_token": "..."
}
```
* Generate the above by doing the following:
   * Go to www.citystrides.com (on Firefox)
   * `Ctrl + Shift + I` to open the Web Developer Tools
   * Choose a city on CityStrides, and click the 'Show Nodes" button (need to subscride for access to nodes)
   * Copy the `GET` command using the `Copy Value` -> `Copy as Curl` 
   * Paste the curl command to https://curlconverter.com/python/
   * Your `cookies` can be found in the generated command
3. You can now run:
   * `./download_node_csv.py cookie.json` to scrape all the nodes to `nodes.csv`
   * `./plot_nodes.py` to view all of the nodes without a 1000 node limit
  
TODO: Add graph algorithm that builds routes. Need to query "path API" though. Straight lines isn't enough.
