# betterBlur
set cut_paste_input [stack 0]
version 10.5 v1
push $cut_paste_input
Group {
 name BLUR3
 selected true
 xpos 2344
 ypos 5937
 addUserKnob {20 User}
 addUserKnob {41 steping T NoOp1.steping}
}
 Input {
  inputs 0
  name Input1
  xpos -40
  ypos 383
 }
 Shuffle {
  name Shuffle8
  xpos -40
  ypos 424
 }
set N50b70000 [stack 0]
 Dot {
  name Dot12
  xpos 109
  ypos 427
 }
set Nfa040000 [stack 0]
 Dot {
  name Dot13
  xpos 219
  ypos 427
 }
set N6e411800 [stack 0]
 Dot {
  name Dot14
  xpos 301
  ypos 427
 }
set N173a9400 [stack 0]
 Dot {
  name Dot15
  xpos 417
  ypos 427
 }
set Nfa040800 [stack 0]
 Dot {
  name Dot16
  xpos 527
  ypos 427
 }
set N18f1b000 [stack 0]
push $N18f1b000
 Blur {
  size {{curve*parent.NoOp1.steping*16*2*2 x1112 1} {curve*parent.NoOp1.steping*16*2*2 x1112 1}}
  name Blur8
  xpos 497
  ypos 532
 }
push $Nfa040800
 Blur {
  size {{curve*parent.NoOp1.steping*16*2 x1112 1} {curve*parent.NoOp1.steping*16*2 x1112 1}}
  name Blur7
  xpos 383
  ypos 532
 }
push $N173a9400
 Blur {
  size {{curve*parent.NoOp1.steping*16 x1112 1} {curve*parent.NoOp1.steping*16 x1112 1}}
  name Blur6
  xpos 267
  ypos 534
 }
push $N6e411800
 Blur {
  size {{curve*parent.NoOp1.steping*4 x1112 1} {curve*parent.NoOp1.steping*4 x1112 1}}
  name Blur5
  xpos 185
  ypos 534
 }
push $Nfa040000
 Blur {
  size {{curve*parent.NoOp1.steping*2 x1112 1} {curve*parent.NoOp1.steping*2 x1112 1}}
  name Blur4
  xpos 75
  ypos 538
 }
push $N50b70000
 Blur {
  size {{curve*parent.NoOp1.steping x1112 1} {curve*parent.NoOp1.steping x1112 1}}
  name Blur3
  xpos -40
  ypos 533
 }
 Merge2 {
  inputs 2
  operation plus
  mix 0.095
  name Merge3
  xpos 75
  ypos 666
 }
 Merge2 {
  inputs 2
  operation plus
  mix 0.4
  name Merge4
  xpos 185
  ypos 666
 }
 Merge2 {
  inputs 2
  operation plus
  mix 0.3
  name Merge5
  xpos 273
  ypos 666
 }
 Merge2 {
  inputs 2
  operation plus
  mix 0.2
  name Merge6
  xpos 383
  ypos 666
 }
 Merge2 {
  inputs 2
  operation plus
  mix 0.1
  name Merge7
  xpos 497
  ypos 666
 }
 Output {
  name Output1
  xpos 497
  ypos 777
 }
 Viewer {
  inputs 2
  frame 1071
  input_process false
  name Viewer1
  xpos 788
  ypos 622
 }
 NoOp {
  inputs 0
  name NoOp1
  xpos -209
  ypos 539
  addUserKnob {20 User}
  addUserKnob {14 steping R 0 100}
  steping {11 11}
 }
end_group

