# NumScope

This project is a customized version of the open-source PhoneInfoga tool, tailored for use in a secure, offline lab environment without the web interface. The main goal of this project was to gather useful intelligence using a phone number as an entry point, as part of reconnaissance training and information gathering in cybersecurity exercises.

🛠 What I Did

- Removed frontend web UI dependencies to allow CLI-only usage.
- Modified the web package (client.go and server.go) to bypass missing client/dist/ errors.
- Built a clean, portable command-line version using Go.
- Learned to scan phone numbers for OSINT data and export results to .txt files for analysis.

🔍 Use Case

This CLI-only version is ideal for:
- Offline or restricted environments where GUI access is limited.
- Cybersecurity labs focused on practicing reconnaissance techniques.
- Analysts or red teamers performing phone-based OSINT without exposing data over the web.


Steps 

1.  Create a Directory and change directory

```bash
mkdir phonerecon && cd phonerecon
```

2. Install Phoneinfoga tool using git

```bash
git clone https://github.com/sundowndev/phoneinfoga.git
```

3. Change directory to phoneinfoga upon completion in the cloning

```bash
cd phoneinfoga
```

4. Edit web/client.go content and replace with content that focus on CLI only build

```bash
vim web/client.go 
```

Delete existing go content

```bash
dG
```

Replace with 

```go

package web

import (
	"github.com/gin-gonic/gin"
)

// Web UI is disabled in CLI-only mode.
// This stub satisfies interface calls without serving static assets.

func registerClientRoutes(router *gin.Engine) error {
	// Do nothing in CLI-only mode
	return nil
}
```







