fun main() {
    fun glavna(step: Int, min: Int, max: Int): Int {
        var niz = IntArray(max/4)
        var b = 0
        var i = 2
        for (izracun in min..max) {
            while (i<(izracun-1))  {
                    if (izracun % i == 0) {
                        break
                    }
                    else {
                        i++
                    }
                }
            if (i == izracun-1) {
                niz[b] = izracun
                b++
            }
            i = 2
            }
            for (a in 0..max / 4) {
                var c = niz[a]
                var d = niz[a] + step
                var g = niz[a+1]
                if (d == g) {
                    println("[$c] [$d]")
                    break
                }
            }
            return b
        }
    glavna(6, 20, 40)
    }
