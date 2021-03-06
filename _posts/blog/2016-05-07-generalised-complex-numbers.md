---
layout: post
title: Generalized Complex Numbers
modified:
categories: blog
excerpt:
tags: [MnP, Summers]
author : anish
comments: true
image:
  feature:
date: 2016-05-17T10:19:07+00:00
---

Have you ever wondered, why is multiplication of complex numbers defined in such a peculiar fashion and can we do it in another way? Can there be other geometrical interpretations for complex numbers? It turns out, these questions are related and lead to the definition of “Generalized Complex Numbers.”

Generalized Complex Numbers:

Here we redefine the multiplication on the set RxR while preserving certain properties. Addition is defined as before. We desire multiplication to be associative, commutative and distributive. Further we want to satisfy:

$$ (x1,y1)*(x,0) = (x*x1,x*y1) $$

This is because we still want to interpret the set {(x,0)| x is real} as “purely real” numbers. Thus we can interpret (x,y) as

(x,y) = (x,0)*(1,0)+(y,0)*(0,1)

The properties of the new multiplication discussed so far allow us to conclude:

(x1,y1)*(x2,y2)= =x1x2 + (0,1)(0,1)y1y2 + (x1y2 + x2y1)(0,1)

Thus, it all boils down to the definition of (0,1)*(0,1) . We may now define:

(0,1)(0,1)=(p,q)

It turns out, there are only three different ways (unique up to isomorphism as rings) to choose p and q. For example, q = 0 and p = 1 , 0 or -1. The choice p = -1 gives us complex numbers that we are familiar with, p = 1 gives double numbers while p = 0 gives dual numbers. From here on we assume q = 0 and p as any real number and the term complex number refers to generalized complex number.

Application of dual numbers:

Here we make a rather strange choice (0,1)2 = (0,0). As a handy notation let ɛ  = (0,1). So every dual number is of the form a+ɛb and ɛ2 = 0. Suppose P(x) is a polynomial over reals. We see that :

P(a+bɛ) = P(a) + bɛP'(a)

Where P' denotes the derivative. In fact this is also true for a power series and hence for any analytical function. For example,

sin(a+bɛ) = sin(a) + bɛcos(a)

This is a technique used in Automatic Differentiation in Computer Algebra.

Geometrical Properties:

Now let us examine a few geometric properties. Define the complex conjugate of (x,y) to be (x,-y) as before. Notice that (x,y)(x,-y) = (x^2 – py^2,0) is always a “real number”. So we define modulus of (x,y) as

|(x,y)| = sqrt(|x^2 –py^2|)

A unit circle is then defined as the set {(x,y) | |(x,y)| = 1} This represents an Ellipse for p<0 (Elliptic number system), a pair of parallel lines for p=0 (Parabolic number system) and a pair of conjugate hyperbolae for p>0 (Hyperbolic Number system). The argument of a complex number T(x,y) is defined as twice the area of the portion of the unit circle cut out by the ray OT and the real axis, O being the origin (this definition isn’t complete. The attached article gives a fuller account). These definitions give us the beautiful result:

The modulus of the product is the product of the modulus; and the argument of the product is the sum of arguments.

|z1z2| = |z1||z2|

Arg(z1z2) = Arg(z1) + Arg(z2)

Geometrically, this means that multiplication by a generalized complex number is a rotation in the respective plane followed by scaling. Multiplication by a unit complex number is just pure rotation.

Application to Special Relativity and Lorentz Transformation:

Consider p=1/c2 and let (t,x) and (t',x') denote the spacetime coordinates of an event in ground frame and a reference frame moving with velocity v w.r.t. it. Let z = (1,v) and w be the unit complex number z/|z|. Then

(t,x)*w =  (t',x')

Thus, the Lorentz transform in two dimensional Special Relativity is a rotation in the hyperbolic complex plane! This means the modulus doesn’t change under this transform. Which means:

(ct)^2 – x^2 = (ct')^2 – x'^2

It is also interesting to note that if p=0, (the case of dual numbers), then w = (1,v) is a unit complex number and multiplication by it gives us the Galilean transformation.

(t,x)*(1,v) = (t, x+vt )

You can find more exciting stuff like trigonometry in various cases (p<0, p=0, p>0) and the generalizations of Euler’s formula in the article. Have fun exploring their properties. If you come to know of any other applications of generalized complex numbers, please do share!
