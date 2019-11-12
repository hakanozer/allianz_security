<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>

<%@ taglib uri="http://java.sun.com/jsp/jstl/core" prefix="c" %>
<%@ taglib uri="http://www.springframework.org/tags/form" prefix="f" %>
<%@ taglib uri="http://www.springframework.org/tags" prefix="s" %>  
    
    
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Insert title here</title>
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
</head>
<body>
<div class="container">
	
	<div class="row">
		<div class="col-sm-4"></div>
		<div class="col-sm-4">
			<h1>User Register</h1>
			<form id="frmRegister" action='<s:url value="/userRegister"></s:url>' method="post" >
				<input name="name" type="text" class="form-control" placeholder="Name" />
				<input name="surname" type="text" class="form-control" placeholder="Surname" />
				<input name="mail" type="text" class="form-control" placeholder="Mail" />
				<input name="pass" type="password" class="form-control" placeholder="Pass" />
				<input type="submit" value="Send" class="btn btn-danger"/>
			</form>
		</div>
		<div class="col-sm-4"></div>
	</div>
	
</div>
</body>
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js" integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js" integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM" crossorigin="anonymous"></script>
<script>

$(document).ready(function () {
	$("#frmRegister").submit(function () {
		var n = $("input[name='name']").val()
		var s = $("input[name='surname']").val()
		if (n === "" || s === "") {
			alert("Lütfen tüm alanları doldurunuz!")
			return false;
		}
		
	})
})

</script>



</html>
