import requests
import json

# Set the repository name and the Personal Access Token
repository = "your_repository_name"
pat = "sp=r&st=2023-01-23T22:15:42Z&se=2023-01-24T06:15:42Z&spr=https&sv=2021-06-08&sr=b&sig=%2BCP2SdxOrzeU53nYIafM5BoBPt87xufpfMt6ym2ZOLo%3D"

# Set the headers for the API call
headers = {
    "Accept": "application/vnd.github+json",
    "Authorization": f"Token {pat}",
}

# Call the GitHub API to create a new code scanning alert
url = f"https://api.github.com/repos/{repository}/code-scanning/alerts"
data = {
    "name": "Test Alert",
    "query": "language:python AND vulnerability",
    "reason": "Testing code scanning feature",
}
response = requests.post(url, headers=headers, json=data)

# Print the response
print(response.json())
