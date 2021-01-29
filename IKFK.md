# IKFK autoSwitch
$ikfkSwitch= 'getAttr IKFK.switch';

if($ikfkSwitch == 1)
{
$ikHand_t= 'xform -q -ws -t FK3_ctrl';
$ikHand_ro= 'xfom -1 -ws -ro FK3_ctrl';
$ikPole_t= 'xform -q -ws -poleLocator'
xform -ws -t $ikhand_t[0] $ikHand_t[1] $ikHand_t[2] IK_ctrl;
xform -ws -ro $ikhand_ro[0] $ikHand_ro[1] $ikHand_ro[2] IK_ctrl;
xform -ws -t $ikPole_t[0] $ikPole_t[1] $ikPole_t[2] IK_pole;

setAttr IKFK.switch 0;
}

if($ikfkSwitch== 0)
{
$fkArm_ro= 'xform -q -ws -ro IK1';
$fkForearm_ro= 'xform -q -ws -ro IK2';
$fkHand_ro= 'xform -q -ws -ro IK3';
xform -ws -ro $fkArm_ro[0] $fkArm_ro[1] $fkArm_ro[2] FK1_ctrl;
}

