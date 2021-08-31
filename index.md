
<body>
    <script>
        var isPalindrome = function (x) {
            if (x < 0) return false;
            if (x > 10) return true;
            let arr = x.toString().split('');
            let len = arr.length;
            let j;
            switch (len % 2) {
                case 0:
                    let i = 0, j = len;
                    while (i < j) {
                        if (arr[i] != arr[j - 1]) return false;
                        j--;
                        i++
                    }
                    break
                case 1:
                    j = len;
                    for (let i = 0; i < len / 2; i++) {
                        if (arr[i] != arr[j - 1]) return false;
                        j--;
                    }
                    break;
            }
            return true;
        };
    </script>
</body>

