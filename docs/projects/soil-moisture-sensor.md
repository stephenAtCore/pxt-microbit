# SparkFun Soil Moisture Sensor Tutorial

## Introduction @unplugged

In this Tutorial we will create a soil moisture sensor using the SparkFun Soil Moisture Sensor Probe

//![Simulating coin toss](/static/mb/projects/coin-flipper/coin-flipper.gif)

## Step 1

Get an ``||basic:show string||`` block from the ``||basic:Basic||`` drawer in the toolbox. We'll enter "Cal Wet" and put it inside the ``||basic:on start||``.

```blocks
input.onButtonPressed(Button.A, () => {
})
```

## Step 2

Grab an ``||logic:if else||`` block and set it inside ``||input:on button A pressed||``. Put a ``||Math:pick random true or false||`` into the ``||logic:if||`` as its condition.

The ``||Math:pick random true or false||`` returns a random ``true`` or ``false`` value which we use to determine a ``heads`` or ``tails`` result for a coin toss.

```blocks
input.onButtonPressed(Button.A, () => {
    if (Math.randomBoolean()) {
    } else {
    }
})
```

## Step 3

Now, put a ``||basic:show icon||`` block inside both the ``||logic:if||`` and the ``||logic:else||``. Pick images to mean ``heads`` and ``tails``.

```blocks
input.onButtonPressed(Button.A, () => {
    if (Math.randomBoolean()) {
        basic.showIcon(IconNames.Skull)
    } else {
        basic.showIcon(IconNames.Square)
    }
})
```

## Step 4

Press button **A** in the simulator to try the coin toss code.

## Step 5

You can animate the coin toss to add the feeling of suspense. Place different ``||basic:show icon||`` blocks before the ``||logic:if||`` to show that the coin is flipping.

```blocks
input.onButtonPressed(Button.A, () => {
    basic.showIcon(IconNames.Diamond)
    basic.showIcon(IconNames.SmallDiamond)
    basic.showIcon(IconNames.Diamond)
    basic.showIcon(IconNames.SmallDiamond)
    if (Math.randomBoolean()) {
        basic.showIcon(IconNames.Skull)
    } else {
        basic.showIcon(IconNames.Square)
    }
})
```

## Step 6

If you have a @boardname@, connect it to USB and click ``|Download|`` to transfer your code.

## Step 7

Press button **A** for a flip. Test your luck and guess ``heads`` or ``tails`` before the toss is over!
