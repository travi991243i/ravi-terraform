# ravi-terraform
#terrafrom
#this includes code for terraform page
<html>
<head> 
<title>Example form</title>
<!-- style section -->

    <style type="text/css">
    .container {
        width: 500px;
        clear: both;
    }
    .container input {
        width: 100%;
        clear: both;
    }
	
	.section-start {}
	.section-end{}
	.section-child-lvl1 {
		margin-left: 25px;
	}

    </style>
</head>
<body>
<div class="container">

      
<!-- // template section -->
	<script id="kumar" type="text/x-jQuery-tmpl">
		
		<div>resource "${res}" "${rn}" {</div>
			<div>ami = "${img}"</div>
			<div>instance_type = "${type}"</div>
			
			<div> count = "${count}" </div>
			<div>disable_api_termination = "${dpt}" </div>
			<div>instance_initiated_shutdown_behavior = "${shutdown}" </div>
			<div>availability_zone = "${albzone}" </div>
			<div>ebs_optimized = "${ebsopt}" </div>
			<div> associate_public_ip_address = "${asspubip}" </div>
			<div>monitoring = "${mont}" </div>
			<div> root_block_device </div>
			<div> { </div>
			<div> volume_type = "${vtype}" </div>
			<div> volume_size = "${vsize}" </div>
			<div> delete_on_termination = "${delonter}" </div>
			<div> } </div>
			
			
			
		<div>}</div>
    </script>
 <!-- //template section(v) -->
 <script id="ravi" type="text/x-jQuery-tmpl">
		
		<div>resource "${res}" "${rn}" {</div>
			<div>cidr_block = "${cdr}"</div>
			<div>instance_tenancy = "${inty}"</div>
			<div> tags { </div>
			<div> name = "${tag}" </div>
			<div> } </div>
		<div>}</div>
    </script>
	<!-- //src section -->
    <script type="text/javascript" src="http://ajax.aspnetcdn.com/ajax/jQuery/jquery-1.4.4.js"></script>
    <script type="text/javascript" src="http://ajax.aspnetcdn.com/ajax/jquery.templates/beta1/jquery.tmpl.js"></script>
	<script src="https://code.jquery.com/jquery-3.1.1.js" ></script>                                                         
<script src="https://code.jquery.com/ui/1.11.4/jquery-ui.js"></script>‌​
 <script type="text/javascript" src="http://ajax.aspnetcdn.com/ajax/jquery.templates/beta1/jquery.tmpl.js"></script>
 
 <!-- //from -->
 
 <!-- <p> <i> create provider file to hide access key and secret key </i> </p> -->
 
<form>
<!-- <label>  Access key  </label>  <input type="text" id="Akey" name="Akey" > <br /> -->

<!-- <label>  Secret Key  </label>  <input type="text" id="Skey" name="Skey" > <br /> -->

<!--//region section 

<label>  Region  </label>     
<select id="reg" name="reg">
  <option value="">Select region</option>
  <option value="us-east-1">us-east-1(US East (N. Virginia))</option>
  <option value="us-east-2	">us-east-2	(US East (Ohio))</option>
  <option value="us-west-1">us-west-1US West (N. California)</option>
  <option value="	us-west-2">	us-west-2 (US West (Oregon))</option>
   <option value="	ap-northeast-2">ap-northeast-2(Asia Pacific (Seoul))</option>                  
    <option value="ap-southeast-1">ap-southeast-1(Asia Pacific (Singapore))</option>
	 <option value="ap-southeast-2">Asia Pacific (Sydney)</option>
	  <option value="ap-northeast-1">ap-northeast-1 (Asia Pacific (Tokyo))</option>
	   <option value="eu-central-1">eu-central-1 (EU (Frankfurt))</option>
	   	   <option value="eu-west-1">eu-west-1 (EU (Ireland))</option>
</select>    <br /> -->

<!--//resource section -->

<label>  Resource  </label>
<select id="res" name="res">
  <option value="">Select resource</option>
  <option value="aws_instance">instance</option>
  <option value="aws_vpc">vpc</option>
  <option value="aws_security_group">security group</option>
  <option value="aws_s3_bucket">s3 bucket</option>
</select>    <br />

 <!--// tags -->
 
<label> tags </label> <input type="text" id="tag" name="tag" > <br />     


<!--// resource -->

<label>  Resource Name </label> <input type="text" id="rn" name="rn" > <br />  

<!--// options declarations -->

<div class="machine_img" id="machine_img" style="display:none;">
  <label>ami</label>
  <input type="text" name="ami" id="img">                                      
</div>

<!-- //instance type section -->
 
<select id="type" name="type">
  <option value="">Select instance type</option>
  <option value="t2.nano">t2.nano</option>
  <option value="t2.micro">t2.micro</option>
  <option value="t2.small	">t2.small	</option>
  <option value="t2.medium">t2.medium</option> 
  <option value="t2.large">t2.large</option>
  <option value="t2.xlarge">t2.xlarge</option>
 <option value="t2.2xlarge">t2.2xlarge</option>
 <option value="m4.large">m4.large</option>
 <option value="m4.xlarge">m4.xlarge</option>
 <option value="m4.2xlarge">m4.2xlarge</option>
 <option value="m4.4xlarge">m4.4xlarge</option>
 <option value="m4.10xlarge">m4.10xlarge</option>                 
 <option value="m4.16xlarge">m4.16xlarge</option>
 <option value="m3.medium	">m3.medium	</option>
 <option value="m3.large">m3.large</option>
 <option value="m3.xlarge">m3.xlarge</option>
 <option value="m3.2xlarge">m3.2xlarge</option>
 <option value="c4.large">c4.large</option>
 <option value="c4.xlarge">c4.xlarge</option>
 <option value="c4.2xlarge">c4.2xlarge</option>
 <option value="c4.4xlarge">c4.4xlarge</option>
 <option value="c4.8xlarge">c4.8xlarge</option>
 <option value="c3.large">c3.large</option>
 <option value="c3.xlarge">c3.xlarge</option>
 <option value="c3.2xlarge">c3.2xlarge</option>
 <option value="c3.4xlarge">c3.4xlarge</option>
 <option value="c3.8xlarge">c3.8xlarge</option>
 <option value="x1.32xlarge	">x1.32xlarge	</option>
 <option value="x1.16xlarge	">x1.16xlarge</option>
 <option value="r4.large">r4.large</option>
 <option value="r4.xlarge">r4.xlarge</option>
 <option value="r4.2xlarge">r4.2xlarge</option>
 <option value="r4.4xlarge">r4.4xlarge</option>
 <option value="r4.8xlarge">r4.8xlarge</option>
 <option value="r4.16xlarge">r4.16xlarge</option>
 <option value="r3.large">r3.large</option>
 <option value="r3.xlarge">r3.xlarge</option>
 <option value="r3.2xlarge">r3.2xlarge</option>
 <option value="r3.4xlarge">r3.4xlarge</option>
 <option value="r3.8xlarge">r3.8xlarge</option>
<option value="p2.xlarge">p2.xlarge</option>
 <option value="p2.8xlarge">p2.8xlarge</option>
 <option value="p2.16xlarge">r4.8xlarge</option>
 <option value="g2.2xlarge	">g2.2xlarge</option>
 <option value="g2.8xlarge">g2.8xlarge</option>
 <option value="f1.2xlarge">f1.2xlarge</option>
 <option value="f1.16xlarge">f1.16xlarge</option>
 <option value="i2.xlarge">i2.xlarge</option>
 <option value="i2.2xlarge">i2.2xlarge</option>
 <option value="i2.4xlarge">i2.4xlarge</option>
 <option value="i2.8xlarge">i2.8xlarge</option>
 <option value="d2.xlarge">d2.xlarge</option>
 <option value="d2.2xlarge">d2.2xlarge</option>
 <option value="d2.4xlarge">d2.4xlarge</option>
 <option value="d2.8xlarge">d2.8xlarge</option> 
</select>    <br />
<label> subnet id </label> <input type=text id="subid" name="subid"> <br />

<label> count </label>  <input type="text" id="count" name="count">  <br />
<label> termination protection </label> <select id="dpt" name="dpt" >
<option value="true">True </option>
<option value="false">False </option>
</select> <br />


<label> Shutdown Behaviour </label> <select id="shutdown" name="shutdown" > 
<option value="stop">stop</option>
<option value="reboot">reboot </option>
<option value="terminate">terminate </option>
</select> <br />

<label> availability_zone </label> <input type="text" id="albzone" > <br />

<label> associate public ip </label> 
<select id="asspubip" name="asspubip" >
<option value="ture"> True </option>
<option value="false"> False </option>
</select>
<br />

<label> Monitoring </label>
<select id="mont" name="mont" >
<option value="true"> True </option>
<option value="false"> False </option>
</select> <br />

<f> root storage declaration </f> <br />

<label> volume type </label>
<select id="vtype" name="vtype" >
<option value="standard">standard </option>
<option value="gp2">gp2 </option>
<option value="io1">io1 </option>
</select>
<br />

<label> volume size in GB</label> <input type="text" id="vsize" name="vsize"> <br />

<label> Delete on termination </label>
<select id="delonter" name="delonter">
<option value="true">true </option>
<option value="false">false </option>
</select> <br />


<!-- network class -->
<div class="network"  id="network" style="display:none;">
  <label>cdir</label>
  <input type="text" name="cdir" id="cdr">
</div>

<!-- tenancy class -->
<div class="vpc_tenancy"  id="vpc_tenancy" style="display:none;">
  <label>tenancy</label>
  <input type="text" name="tenancy" id="inty">
</div>


<input type="button" id="submit" name="submit" value="Submit"/>
</form>

<div id='gen-json'>
</div>

<!-- template generation -->



<script type="text/javascript">
$("#create").click(function () {
var data={'Akey' : $('#Akey').val(),'Skey' : $('#Skey').val(),'reg' : $('#reg').val() };
$('#gen-json').html();
$('#gen-json').append($("#create").tmpl(data));
});
</script>

<script type="text/javascript">
	$("#submit").click(function(){
	if( $('#res').val()== "aws_instance" )
	{
		var data={'Akey' : $('#Akey').val(),'Skey' : $('#Skey').val(),'reg' : $('#reg').val(),'res' : $('#res').val(),'rn' : $('#rn').val(),'img' : $('#img').val(),'type' : $('#type').val(), 'sid' : $('#sid').val(), 'sg' : $('#sg').val(), 'tag' : $('#tag').val(), 'count' : $('#count').val(), 'dpt' : $('#dpt').val(), 'shutdown' : $('#shutdown').val(), 'albzone' : $('#albzone').val(), 'asspubip' : $('#asspubip').val(), 'mont' : $('#mont').val(), 'vtype' : $('#vtype').val(), 'vsize' : $('#vsize').val(), 'delonter' : $('#delonter').val() };

		//console.log(data);
		//console.log($("#bookTemplate").tmpl(data));
		$('#gen-json').html('');
		$('#gen-json').append($("#kumar").tmpl(data));
		}
		else // else used for vpc
		{
		var data={'Akey' : $('#Akey').val(),'Skey' : $('#Skey').val(),'reg' : $('#reg').val(),'res' : $('#res').val(),'rn' : $('#rn').val(),'img' : $('#img').val(),'type' : $('#type').val(), 'sid' : $('#sid').val(), 'sg' : $('#sg').val(), 'tag' : $('#tag').val(), 'cdr' : $('#cdr').val(), 'inty' : $('#inty').val() };
		$('#gen-json').html('');
		$('#gen-json').append($("#ravi").tmpl(data));
		}
	});
	</script>
	
	<!-- button section -->
	
	<script type="text/javascript">
$('#res').on('change',function(){
        if( $(this).val()=="aws_instance"){
        $("#machine_img").show();                  // instance button
        $("#type").show();
        $("#network").hide();
        $("#vpc_tenancy").hide();
        }
        else if($(this).val()=="aws_vpc"){
        	$("#network").show();
        	$("#vpc_tenancy").show();           // vpc button show
          $("#machine_img").hide();
        $("#type").hide();
        }
        else{
        $("#machine_img").hide();
        $("#type").hide();
        $("#network").hide();
        $("#vpc_tenancy").hide();
        }
    });
</script>
</div>
</body>
</html>
