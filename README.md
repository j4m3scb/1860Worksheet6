# 1860Worksheet6

CHIP A6Q2201817059 {
IN a, b, c, d;
OUT f;
PARTS:
Not (in=a, out=nota);
Not (in=b, out=notb);
Not (in=c, out=notc);
Not (in=d, out=notd);
And (a=nota, b=notb, out=or1);
And (a=or1, b=notc, out=or2);
And (a=or2, b=d, out=out1);
And (a=nota, b=b, out=or1);
And (a=or1, b=notc, out=or2);
And (a=or2, b=d, out=out2);
And (a=nota, b=b, out=or1);
And (a=or1, b=c, out=or2);
And (a=or2, b=notd, out=out3);
And (a=a, b=notb, out=or1);
And (a=or1, b=notc, out=or2);
And (a=or2, b=d, out=out4);
And (a=a, b=notb, out=or1);
And (a=or1, b=c, out=or2);
And (a=or2, b=notd, out=out5);
Or (a=out1, b=out2, out=and1);
Or (a=and1, b=out3, out=and2);
Or (a=and2, b=out4, out=and3);
Or (a=and3, b=out5, out=f);
}