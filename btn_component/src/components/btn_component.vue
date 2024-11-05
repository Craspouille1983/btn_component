<template>
    <button>
        <svg>
            <rect x="1" y="1" rx="30"></rect>
        </svg>
        {{ modelValue }}
    </button>
</template>

<script>
export default {
    name: 'buttonComponent',
    props: {
        modelValue: {
            type: String,
            default: 'Bouton'
        }
    }
}
</script>
<style scoped>
button {
    margin-top: 3em;
    display: inline-block;
	position: relative;
    width: fit-content;
    font-family: 'Pangolin', cursive;
    padding: .5rem 1.25rem;
    color: white;
    border: none;
	line-height: 2.5em;
	background: rgba(3, 3, 3, 1);
	border-radius: 2rem;
	font-size: 1.25em;
	text-transform: uppercase;
	text-decoration: none;
	text-align: center;
	-webkit-text-stroke: 1px rgba(255, 255, 255, 1);
	-webkit-text-fill-color: white;
	transition: 0s;
	svg {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		rect {
			position: absolute;
			top: 0;
			left: 0;
			stroke-width: 3;
			stroke: rgba(0, 255, 0, 1);
			fill: none;
			width: 100%;
			height: calc(100% - 2px);
			stroke-dasharray: 600;
			stroke-dashoffset: -600;
			transition: .75s;
		}
	}
	&::before {
		content: "";
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		left: 0;
		transition: 0;
		border-radius: 40px;
	}
	&:hover {
		transition: -webkit-text-stroke .5s, -webkit-text-fill-color .75s, .5s;
		transition-delay: 1s;
		background: rgba(0, 255, 0, 1);
		color: rgba(0, 28, 31, 1);
		-webkit-text-fill-color: rgba(0, 28, 31, 1);
		-webkit-text-stroke: 1px transparent;
	}
	&:hover::before {
		transition: .5s;
		transition-delay: 1s;
		box-shadow: 0 0 1.8em rgba(0, 255, 0, 1), 
					0 0 2.5em rgba(0, 255, 0, 1);
	}
	&:hover svg rect {
		stroke-dasharray: 600;
		stroke-dashoffset: 0;
	}
}
</style>