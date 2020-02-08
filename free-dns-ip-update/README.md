
# IP Update for freedns.afraid.org

Script to update a dynamic ip on freedns.afraid.org. It requires an account on freedns.afraid.org and a Direct URL. It uses ifconfig.io to determine the current ip address.

Note: It will only call freedns.afraid.org if the ip address has changed.

## Get started

1. Create a free account at freedns.afraid.org
2. Configure a free Dynamic DNS address
3. Store the Direct URL in the file .url in the same directory as the ip.sh script
4. Run the script

```shell
./ip.sh
```

To automate with crontab:

```shell
sudo crontab -e

# Run at 3 and 33 minutes past the hour. Adjust as needed.
3,33 * * * * [absolute path to script]/ip.sh >> [absolute path to script]/ip.log

```

## Details

After a successful run, the following files are generated:

```shell
.ip         # the current public ip address
.lastrun    # the last time the script was executed
.lastupdate # the last time the script called freedns.afraid.org to update
```

## License

```text
MIT License

Copyright (c) 2020 Jared Willden

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
