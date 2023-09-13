<script>
	// Get the current date and month
	const date = new Date();
	const currentMonth = date.getMonth() + 1; // months are 0-based

	// Define the path to the image
	const imagePath = `/images/monthly_kortejarvi/${currentMonth}.jpg`;
</script>

<img
	src={imagePath}
	alt="Kuukausittainen kuva Lempäälän Kortejärveltä"
	class="absolute top-0 left-0 w-full h-full object-cover object-center -z-10"
/>
