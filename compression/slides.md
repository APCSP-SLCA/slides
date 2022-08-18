---
marp: true
theme: uncover
author: Joshua Bas
math: katex
---

# **Information Layer**

AP CSP @ SouthLake Christian Academy

---

We saw that simple messages, colors, and images require many bits.

EX: A 1200x1200 pixel 24-bit color emoji requires

$$ 1200 \times 1200 \times 24 = 34560000 \text{ bits} = 4320000 \text{ bytes} $$

$$ = 4320000 \text{ bytes}$$

![demo width:100px](emoji.png)

---

<style scoped>
    section {
        background: #020c17;
    }
</style>

![bg contain](emoji_size.png)

---

## **Compression**

* **lossy**: compression that *loses information*
    * data gets trashed to save space
    * unable to reconstruct original data
* **lossless**: compression that does not loses information
    * able to reconstruct original data

---

## **Run Length Encoding**

* a method of compression that describes how many times a character or text is repeated

* starting from left to right, we start counting how many times `1` is repeated, then how many times `0` is repeated, etc.


Instead of `000001111111` &rarr; `0 5 7`

---

![brick](brick.avif)

---

![compressed brick](brick_compressed.avif)

Which type of compression?

---

<div style="display: grid; grid-template-columns: 1fr 1fr; grid-gap: 75px; margin: auto auto;">
    <img src="nyan.PNG" style="width:250px;">
    <img src="nyan_compressed.PNG" style="width:250px;">
    <span style="margin-left:auto auto;">Size: 12KB</span>
    <span style="margin-left:auto auto;">Size: 4KB</span>
</div>

Which type of compression?

---

### Takeaway

* Run Length encoding is a *lossless* compression
* *Lossy* compression generally allows for faster transmission
    * since we threw out bits, we can send a message in less time 

---

## **Quantifying Compression**

**compression rate**: $1 - \cfrac{\text{compressed data size}}{\text{original data size}}$

also called *space saving*

<br><br>

| original size | compressed size | compression rate|
|---------------|-----------------|-----------------|
| 12KB          | 4KB             | $1 -\cfrac{4}{12} \approx 67\%$

---

### *Example*

<style scoped>
    section > table {
        font-size: 80%;
    }
</style>

| original bin     | compressed dec | compressed bin  | compression rate          |
|------------------|----------------|-----------------|---------------------------|
| `0b000001111111` | `0 5 7`        | `0b000101111` | $1 -\frac{9}{12} = 25\%$    |


---

### **Key Takeaways**

1. Compressing data saves us bits!
2. Compression can remove unnecessary data (**lossy**)
    * generally faster transmission speed
3. Compression can just restructure data (**lossless**)
4. Compression methods work better for large data