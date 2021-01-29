# IKFK autoSwitch
$ikfkSwitch= 'getAttr IKFK.switch';

if($ikfkSwitch == 1)
{
$ikHand_t= 'xform -q -ws -t FK3_ctrl';
$ikHand_ro= 'xfom -1 -ws -ro FK3_ctrl';
xform -ws -t $ikhand_t[0] $ikHand_t[1] $ikHand_t[2] IK_ctrl;
xform -ws -ro $ikhand_ro[0] $ikHand_ro[1] $ikHand_ro[2] IK_ctrl;

$ikPole_t= 'xform -q -ws -poleLocator'
xform -ws -t $ikPole_t[0] $ikPole_t[1] $ikPole_t[2] IK_pole;

setAttr IKFK.switch 0;
}

if($ikfkSwitch== 0)
{

}

