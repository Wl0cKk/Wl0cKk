<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Wl0cKk&rank_icon=github&show_icons=true&theme=tokyonight" alt="github stats" width="400"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Wl0cKk&theme=tokyonight&size_weight=0.1&count_weight=0.2&layout=compact" alt="Top Langs" width="300"/>
</p>
<div align="center">
    <div style="display: flex; flex-wrap: nowrap; justify-content: center;">
        <div style="display: flex; flex-wrap: wrap; width: 400px;">
            <div style="flex: 1;">
                <img src="https://skillicons.dev/icons?i=linux" alt="Linux" width="40" height="40" />  
                <img src="https://skillicons.dev/icons?i=ubuntu" alt="Ubuntu" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=kali" alt="Kali" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=debian" alt="Debian" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=mint" alt="Mint" width="40" height="40" />
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3f/Fedora_logo.svg/267px-Fedora_logo.svg.png?20091128031656" alt="Fedora" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=redhat" alt="Red Hat" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=apple" alt="MacOS" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=ruby" alt="Ruby" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=c" alt="C" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=cpp" alt="C++" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=ts" alt="TypeScript" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=lua" alt="Lua" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=bash" alt="Bash" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=python" alt="Python" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=html" alt="HTML" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=css" alt="CSS" width="40" height="40" />
            </div>
            <div style="flex: 1;">
                <img src="https://skillicons.dev/icons?i=docker" alt="Docker" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=git" alt="Git" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=ansible" alt="Ansible" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=postgres" alt="PostgreSQL" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=sqlite" alt="SQLite" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=nginx" alt="Nginx" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=grafana" alt="Grafana" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=postman" alt="Postman" width="40" height="40" />
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQFwBIzoVFfmX3NPoSIrbGhmCXb4KDgbnZKA1zFltVc9tcpOjELPV1U37sGNf3l0W_gzCs&usqp=CAU" alt="Insomnia" width="40" height="40" />
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c6/Wireshark_icon_new.png/600px-Wireshark_icon_new.png?20230509085415" alt="Wireshark" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=arduino" alt="Arduino" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=raspberrypi" alt="Raspberry Pi" width="40" height="40" />
                <img src="https://cdn-bdkok.nitrocdn.com/zASfOZhMHRaGYpKaSOphFIhUcxxDXZOx/assets/images/optimized/rev-c608007/www.tshirtgeek.com.br/wp-content/uploads/2021/09/ELE013-600x600.jpg" alt="ESP32" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=vscodium" alt="VSCodium" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=sublime" alt="Sublime" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=autocad" alt="AutoCAD" width="40" height="40" />
                <img src="https://skillicons.dev/icons?i=blender" alt="Blender" width="40" height="40" />
            </div>
        </div>
    </div>
</div>
</br></br>
<div align="center" style="margin-top: 20px;">
    <a href="https://www.linkedin.com/in/uladzimir-kandratsiuk-b77505295/" target="_blank" style="text-decoration: none;">
        <img src="https://img.shields.io/badge/LinkedIn-282C34?logo=linkedin&logoColor=0077B5" alt="LinkedIn logo" title="LinkedIn" height="30"/></a>
    <a href="https://leetcode.com/u/amnesia10/" target="_blank" style="text-decoration: none;">
        <img src="https://img.shields.io/badge/LeetCode-282C34?logo=leetcode&logoColor=FFA116" alt="LeetCode logo" title="LeetCode" height="30"/></a>
    <a href="https://gist.github.com/Wl0cKk" target="_blank" style="text-decoration: none;">
        <img src="https://img.shields.io/badge/GitHub%20Gist-282C34?logo=github&logoColor=white" alt="GitHub Gist logo" title="GitHub Gist" height="30" /></a>
</div>
</br>

# [664. Strange Printer](https://leetcode.com/problems/strange-printer/description/?envType=daily-question&envId=2024-08-21)
```ruby
# @param {String} s
# @return {Integer}
def strange_printer(s)
    dp = Array.new(101) { Array.new(101, -1) }
    pr = ->(i, j) {
        return 1 if i == j
        return 0 if i > j
        return dp[i][j] if dp[i][j] != -1
        return pr.(i + 1, j) if s[i] == s[i + 1]
        return pr.(i, j - 1) if s[j] == s[j - 1] || s[i] == s[j]
        ans = 2147483647
        (i + 1..j).each { |k| ans = [ans, pr.(i, k - 1) + pr.(k, j)].min }
        dp[i][j] = ans
    }
    return pr.(0, s.length - 1)
end
