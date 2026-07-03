# TryHackMe Day 46–47: Data Representation

## Room Information

**Room:** Data Representation  
**Platform:** TryHackMe  
**Difficulty:** Beginner  
**Focus Area:** Binary, Hexadecimal, Octal, Color Representation, Computer Data Storage

---

## Overview

In this room, I learned how computers represent and store information using binary values. Since computers only understand two states (0 and 1), everything from numbers and colors to images and files must be translated into binary form.

The room explained how colors are represented using RGB values, how binary and hexadecimal numbering systems work, and why understanding these concepts is important in cybersecurity and computing.

---

## Learning Objectives

By completing this room, I learned how to:

- Understand how computers represent colors
- Learn the concept of bits and bytes
- Convert between decimal and binary numbers
- Understand hexadecimal notation
- Learn the basics of octal numbers
- Understand how computer systems store and process data

---

## Why Data Representation Matters

Computers operate using electrical states that can only represent two values:

- 0 (Off)
- 1 (On)

Everything displayed on a computer screen, including:

- Images
- Videos
- Text
- Audio
- Programs

must eventually be stored and processed as binary data.

Understanding data representation is fundamental for cybersecurity professionals because many tools, logs, memory dumps, network packets, and forensic investigations involve binary and hexadecimal values.

---

# Representing Colors

## RGB Color Model

Computers create colors using three primary colors:

- Red (R)
- Green (G)
- Blue (B)

By combining different intensities of these colors, millions of unique colors can be generated.

---

## Representing 8 Colors

If each color can only be:

- On (1)
- Off (0)

then we can represent:

2 × 2 × 2 = 8 colors

Each color is represented using 3 bits.

| Binary | Color |
|----------|----------|
| 000 | Black |
| 001 | Blue |
| 010 | Green |
| 011 | Cyan |
| 100 | Red |
| 101 | Magenta |
| 110 | Yellow |
| 111 | White |

This demonstrates how binary values can represent visual information.

---

## Representing Over 16 Million Colors

Modern systems do not limit colors to simple ON/OFF states.

Each RGB color channel uses:

- 8 bits (1 byte)

Since each channel can represent:

256 values

The total number of possible colors becomes:

256 × 256 × 256

= 16,777,216 colors

This is known as 24-bit color.

---

## Bits and Bytes

### Bit

A bit (binary digit) is the smallest unit of data.

A bit can only be:

- 0
- 1

---

### Byte

A byte consists of:

8 bits

Examples:

| Bits | Decimal Value |
|--------|--------|
| 00000000 | 0 |
| 00000001 | 1 |
| 11111111 | 255 |

A single byte can represent 256 unique values.

---

# Hexadecimal Representation

Working directly with long binary values can be difficult.

For example:

```text
101000111110101000101010
```

Hexadecimal makes this easier:

```text
A3EA2A
```

---

## Why Hexadecimal is Useful

Every hexadecimal digit represents:

4 bits

| Hex | Binary |
|------|---------|
| 0 | 0000 |
| 1 | 0001 |
| 2 | 0010 |
| 3 | 0011 |
| 4 | 0100 |
| 5 | 0101 |
| 6 | 0110 |
| 7 | 0111 |
| 8 | 1000 |
| 9 | 1001 |
| A | 1010 |
| B | 1011 |
| C | 1100 |
| D | 1101 |
| E | 1110 |
| F | 1111 |

---

## Hex Colors

Websites and graphic applications commonly use hexadecimal colors.

Examples:

| Color | Hex Value |
|---------|---------|
| Black | #000000 |
| White | #FFFFFF |
| Red | #FF0000 |
| Green | #00FF00 |
| Blue | #0000FF |

Hexadecimal notation makes color representation more compact and readable.

---

# Number Systems

## Decimal System (Base 10)

Humans use the decimal system because we naturally count using ten fingers.

Digits:

```text
0–9
```

Example:

```text
213
```

Can be expressed as:

```text
2 × 10² + 1 × 10¹ + 3 × 10⁰
```

---

## Binary System (Base 2)

Computers use binary because electronic circuits naturally operate in two states.

Digits:

```text
0 and 1
```

Example:

```text
1001
```

Conversion:

```text
1×2³ + 0×2² + 0×2¹ + 1×2⁰

= 8 + 0 + 0 + 1

= 9
```

---

## Common Binary Values

| Binary | Decimal |
|----------|----------|
| 0000 | 0 |
| 0001 | 1 |
| 0010 | 2 |
| 0011 | 3 |
| 0100 | 4 |
| 0101 | 5 |
| 0110 | 6 |
| 0111 | 7 |
| 1000 | 8 |
| 1001 | 9 |
| 1010 | 10 |
| 1111 | 15 |

---

# Hexadecimal Numbers

Hexadecimal uses:

Base 16

Digits:

```text
0–9
A–F
```

Where:

| Decimal | Hex |
|-----------|-----|
| 10 | A |
| 11 | B |
| 12 | C |
| 13 | D |
| 14 | E |
| 15 | F |

---

## Converting Hexadecimal to Decimal

Example:

```text
9BDF
```

Calculation:

```text
9 × 16³ +
11 × 16² +
13 × 16¹ +
15 × 16⁰
```

Result:

```text
39,903
```

This demonstrates how hexadecimal values can represent large numbers in a compact format.

---

# Octal Numbers

The octal system uses:

Base 8

Digits:

```text
0–7
```

Each octal digit represents:

3 bits

| Octal | Binary |
|---------|---------|
| 0 | 000 |
| 1 | 001 |
| 2 | 010 |
| 3 | 011 |
| 4 | 100 |
| 5 | 101 |
| 6 | 110 |
| 7 | 111 |

---

## Example Octal Conversion

Octal:

```text
357
```

Conversion:

```text
3 × 8² +
5 × 8¹ +
7 × 8⁰
```

Result:

```text
239
```

Although octal is less commonly used today, it still appears in some Linux and Unix environments.

---

# Key Concepts Learned

| Concept | Description |
|-----------|-------------|
| Bit | Smallest unit of data (0 or 1) |
| Byte | 8 bits |
| Binary | Base-2 numbering system |
| Decimal | Base-10 numbering system |
| Hexadecimal | Base-16 numbering system |
| Octal | Base-8 numbering system |
| RGB | Color model using Red, Green, and Blue |
| Hex Color | Compact representation of RGB colors |

---

# Skills Gained

- Binary Number Conversion
- Hexadecimal Fundamentals
- Octal Number Understanding
- Color Representation Concepts
- Data Storage Fundamentals
- Computer Architecture Basics
- Cybersecurity Data Interpretation
- Technical Problem Solving

---

## Completion Badge

![Data Representation](../../assets/data-representation.jpg)

---

# Key Takeaways

- Computers represent all information using binary values.
- A bit can only contain 0 or 1.
- Eight bits make one byte.
- RGB values allow computers to display over 16 million colors.
- Hexadecimal simplifies working with binary data.
- Binary and hexadecimal are widely used in cybersecurity.
- Understanding number systems is essential for networking, programming, digital forensics, and security analysis.

---

# Reflection

This room helped me understand what happens behind the scenes when computers display colors, store information, and perform calculations. Learning how binary, hexadecimal, and octal systems work gave me a stronger foundation for future cybersecurity topics such as networking, programming, digital forensics, malware analysis, and packet inspection.

Understanding data representation is an essential skill because many cybersecurity tools and logs rely heavily on binary and hexadecimal values. This room reinforced the importance of knowing how computers interpret and process information at a low level.

---

**Platform:** TryHackMe  
**Room:** Data Representation  
**Completed:** Day 46–47 of My Cybersecurity Learning Journey
